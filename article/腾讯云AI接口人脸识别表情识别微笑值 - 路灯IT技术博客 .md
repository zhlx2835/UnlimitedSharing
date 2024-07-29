package com.xurui.app;-
-
-
import com.alibaba.fastjson.JSON;-
import com.alibaba.fastjson.JSONArray;-
import com.alibaba.fastjson.JSONObject;-
import com.google.gson.Gson;-
-
import javax.crypto.Mac;-
import javax.crypto.spec.SecretKeySpec;-
import java.io.ByteArrayOutputStream;-
import java.io.IOException;-
import java.io.InputStream;-
import java.io.OutputStream;-
import java.net.HttpURLConnection;-
import java.net.URL;-
import java.net.URLEncoder;-
import java.security.MessageDigest;-
import java.text.SimpleDateFormat;-
import java.util.Date;-
import java.util.HashMap;-
import java.util.Map;-
import java.util.TimeZone;-
-
_/\*\*-
__\*_ _人脸识别：微笑情况-
__\*/-
_public class Iai {-
-
 private static String _SecretId_ \= "xxx";-
private static String _SecretKey_ \= "xx";-
-
private static String _Url_ \= "https://iai.tencentcloudapi.com";-
 //规范请求串-
 private static String _HTTPRequestMethod_ \= "POST";-
private static String _CanonicalURI_ \= "/";-
private static String _CanonicalQueryString_ \= "";-
private static String _CanonicalHeaders_ \= "content-type:application/json; charset=utf-8\\nhost:iai.tencentcloudapi.com\\n";-
private static String _SignedHeaders_ \= "content-type;host";//参与签名的头部信息-
-
 //签名字符串-
 private static String _Algorithm_ \= "TC3-HMAC-SHA256";-
private static String _Service_ \= "iai";-
private static String _Stop_ \= "tc3\_request";-
-
 //版本-
 public static String _Version_ \= "2020-03-03";-
public static String _Region_ \= "ap-beijing";-
-
-
 _/\*\*\*-
__\*_ _示例名片请求方法-
_ _\*_ **_@param_** _args-
_ _\*/-
_public static void main(String\[\] args) {-
 Map<String, Object> params = new HashMap<>();-
// params.put("Image", "data:image/png;base64,");-
 params.put("Url", "https://img1.baidu.com/it/u=420589444,1162154328&fm=26&fmt=auto&gp=0.jpg");-
 params.put("NeedFaceAttributes", 1);-
-
 Gson gson = new Gson();-
 String param = gson.toJson(params);-
 //发送请求 本地封装的https 请求-
 String response = _getAuthTC3_("DetectFace", param, _Version_);-
 //打印请求数据-
 System._out_.println(response);-
 JSONObject object = JSON._parseObject_(response);-
 object = (JSONObject) object.get("Response");-
 JSONObject error = (JSONObject) object.get("Error");-
if (null \== error) {-
 JSONArray array = (JSONArray) object.get("FaceInfos");-
 object = (JSONObject) array.get(0);-
 object = (JSONObject) object.get("FaceAttributesInfo");-
 Integer expression = (Integer) object.get("Expression");-
-
 // ((JSONObject) ((JSONArray) ((JSONObject) object.get("Response")).get("FaceInfos")).get(0)).get("Expression");-
 // Integer i = Integer.parseInt(((JSONObject) ((JSONArray) ((JSONObject) object.get("Response")).get("FaceInfos")).get(0)).get("Expression")+"");- System._out_.println(expression);-
 }else {-
 System._out_.println("随机生成一个值："+99);-
 }-
 }-
-
 _/\*\*-
__ \* v3__鉴权-
_ _\*-
__\*_ **_@param_** _action __方法名-
_ _\*_ **_@param_** _paramJson_ _json__化的参数-
_ _\*_ **_@param_** _version_ _版本号_ _2018-03-01-
__\*_ **_@return-
_** _\*/-
_public static String getAuthTC3(String action, String paramJson, String version) {-
 try {-
 String hashedRequestPayload = _HashEncryption_(paramJson);-
 String CanonicalRequest =-
 _HTTPRequestMethod_ \+ '\\n' +-
 _CanonicalURI_ \+ '\\n' +-
 _CanonicalQueryString_ \+ '\\n' +-
 _CanonicalHeaders_ \+ '\\n' +-
 _SignedHeaders_ \+ '\\n' +-
 hashedRequestPayload;-
 //时间戳-
 Date date = new Date();-
 //微秒\->秒-
 String timestamp = String._valueOf_(date.getTime() / 1000);-
-
 //格林威治时间转化-
 SimpleDateFormat formatter = new SimpleDateFormat("yyyy-MM-dd");-
 formatter.setTimeZone(TimeZone._getTimeZone_("GMT+0"));-
 String dateString = formatter.format(date.getTime());-
-
 //签名字符串-
 String credentialScope = dateString + "/" \+ _Service_ \+ "/" \+ _Stop_;-
 String hashedCanonicalRequest = _HashEncryption_(CanonicalRequest);-
 String stringToSign = _Algorithm_ \+ "\\n" +-
 timestamp + "\\n" +-
 credentialScope + "\\n" +-
 hashedCanonicalRequest;-
-
 //计算签名-
 byte\[\] secretDate = _HashHmacSha256Encryption_(("TC3" \+ _SecretKey_).getBytes("UTF-8"), dateString);-
 byte\[\] secretService = _HashHmacSha256Encryption_(secretDate, _Service_);-
 byte\[\] secretSigning = _HashHmacSha256Encryption_(secretService, _Stop_);-
-
 //签名字符串-
 byte\[\] signatureHmacSHA256 = _HashHmacSha256Encryption_(secretSigning, stringToSign);-
-
 StringBuilder builder = new StringBuilder();-
for (byte b : signatureHmacSHA256) {-
 String hex = Integer._toHexString_(b & 0xFF);-
if (hex.length() == 1) {-
 hex = '0' \+ hex;-
 }-
 builder.append(hex);-
 }-
 String signature = builder.toString().toLowerCase();-
 //组装签名字符串-
 String authorization = _Algorithm_ \+ ' ' +-
 "Credential=" \+ _SecretId_ \+ '/' \+ credentialScope + ", " +-
 "SignedHeaders=" \+ _SignedHeaders_ \+ ", " +-
 "Signature=" \+ signature;-
-
 //创建header 头部-
 Map<String, String> headers = new HashMap<>();-
 headers.put("Authorization", authorization);-
 headers.put("Host", "iai.tencentcloudapi.com");-
 headers.put("Content-Type", "application/json; charset=utf-8");-
 headers.put("X-TC-Action", action);-
 headers.put("X-TC-Version", version);-
 headers.put("X-TC-Timestamp", timestamp);-
 headers.put("X-TC-Region", _Region_);-
 //request 请求-
 String response = _resquestPostData_(_Url_, paramJson, headers);-
return response;-
 } catch (Exception e) {-
 return e.getMessage();-
 }-
 }-
-
 /\*-
\* Function : 发送Post请求到服务器-
 \* Param : params请求体内容，encode编码格式-
 \*/- public static String resquestPostData(String strUrlPath, String data, Map<String, String> headers) {-
 try {-
 URL url = new URL(strUrlPath);-
 HttpURLConnection httpURLConnection = (HttpURLConnection) url.openConnection();-
 httpURLConnection.setConnectTimeout(3000); //设置连接超时时间-
 httpURLConnection.setDoInput(true); //打开输入流，以便从服务器获取数据-
 httpURLConnection.setDoOutput(true); //打开输出流，以便向服务器提交数据-
 httpURLConnection.setRequestMethod("POST"); //设置以Post方式提交数据-
 httpURLConnection.setUseCaches(false); //使用Post方式不能使用缓存-
 //设置header-
 if (headers.isEmpty()) {-
 //设置请求体的类型是文本类型-
 httpURLConnection.setRequestProperty("Content-Type", "application/json; charset=utf-8");-
 } else {-
 for (Map.Entry<String, String> entry : headers.entrySet()) {-
 String key = entry.getKey();-
 String value = entry.getValue();-
 httpURLConnection.setRequestProperty(key, value);-
 }-
 }-
 //设置请求体的长度-
 httpURLConnection.setRequestProperty("Content-Length", String._valueOf_(data.length()));-
-
 //获得输出流，向服务器写入数据-
 if (data != null) {-
 byte\[\] writebytes = data.getBytes();-
 // 设置文件长度-
 OutputStream outputStream = httpURLConnection.getOutputStream();-
 outputStream.write(data.getBytes());-
 outputStream.flush();-
 }-
 int response = httpURLConnection.getResponseCode(); //获得服务器的响应码-
 if (response == HttpURLConnection._HTTP\_OK_) {-
 InputStream inptStream = httpURLConnection.getInputStream();-
return _dealResponseResult_(inptStream); //处理服务器的响应结果-
 }-
 } catch (IOException e) {-
 return "err: " \+ e.getMessage().toString();-
 }-
 return "-1";-
 }-
-
 /\*-
\* Function : 封装请求体信息-
 \* Param : params请求体内容，encode编码格式-
 \*/- public static StringBuffer getRequestData(Map<String, String> params, String encode) {-
 StringBuffer stringBuffer = new StringBuffer(); //存储封装好的请求体信息-
 try {-
 for (Map.Entry<String, String> entry : params.entrySet()) {-
 stringBuffer.append(entry.getKey())-
 .append("=")-
 .append(URLEncoder._encode_(entry.getValue(), encode))-
 .append("&");-
 }-
 stringBuffer.deleteCharAt(stringBuffer.length() - 1); //删除最后的一个"&"-
 } catch (Exception e) {-
 e.printStackTrace();-
 }-
 return stringBuffer;-
 }-
-
 /\*-
\* Function : 处理服务器的响应结果（将输入流转化成字符串）-
 \* Param : inputStream服务器的响应输入流-
 \*/- public static String dealResponseResult(InputStream inputStream) {-
 String resultData = null; //存储处理结果-
 ByteArrayOutputStream byteArrayOutputStream = new ByteArrayOutputStream();-
 byte\[\] data = new byte\[1024\];-
int len = 0;-
try {-
 while ((len = inputStream.read(data)) != -1) {-
 byteArrayOutputStream.write(data, 0, len);-
 }-
 } catch (IOException e) {-
 e.printStackTrace();-
 }-
 resultData = new String(byteArrayOutputStream.toByteArray());-
return resultData;-
 }-
-
-
 _/\*\*-
_ _\*-_ _\*/-_private static String HashEncryption(String s) throws Exception {-
 MessageDigest sha = MessageDigest._getInstance_("SHA-256");-
 sha.update(s.getBytes());-
 //替换java DatatypeConverter.printHexBinary(d).toLowerCase()-
 StringBuilder builder = new StringBuilder();-
for (byte b : sha.digest()) {-
 String hex = Integer._toHexString_(b & 0xFF);-
if (hex.length() == 1) {-
 hex = '0' \+ hex;-
 }-
 builder.append(hex);-
 }-
 return builder.toString().toLowerCase();-
 }-
-
 private static byte\[\] HashHmacSha256Encryption(byte\[\] key, String msg) throws Exception {-
 Mac mac = Mac._getInstance_("HmacSHA256");-
 SecretKeySpec secretKeySpec = new SecretKeySpec(key, mac.getAlgorithm());-
 mac.init(secretKeySpec);-
return mac.doFinal(msg.getBytes("UTF-8"));-
 }-
-
}-

-

本文转自 [https://www.eqishare.com/programming/10.html](https://www.eqishare.com/programming/10.html)，如有侵权，请联系删除。