-
\[code\]-
-
 /\*\*-
 \* 获取在线图片/音频BASE64格式-
 \*-
 \* @param filePath 图片/音频路径-
 \* @return 图片base64位-
 \*/-
 public String base64File(String filePath) {-
 String str = "";-
 try {-
 URL url = new URL(filePath);-
 //SSL请求地址-
 trustAllHttpsCertificates();-
 HttpsURLConnection.setDefaultHostnameVerifier(hv);-
-
-
 HttpURLConnection conn = (HttpURLConnection) url.openConnection();-
 DataInputStream in = new DataInputStream(conn.getInputStream());-
 ByteArrayOutputStream out = new ByteArrayOutputStream();-
 byte\[\] buffer = new byte\[1024 \* 4\];-
 int n = 0;-
 while ((n = in.read(buffer)) != -1) {-
 out.write(buffer, 0, n);-
 }-
 byte\[\] data = out.toByteArray();-
 BASE64Encoder encoder = new BASE64Encoder();-
 str = encoder.encode(data);-
 str = str.replaceAll("\\r|\\n", "");-
 } catch (Exception e) {-
 throw new ValidatorException(StatusCodeEnum.UNKNOW, "媒体资源获取失败！");-
 }-
 return str;-
 }-
-
-
 /\*\*-
 \* 兼容SSL地址请求-
 \*/-
 HostnameVerifier hv = new HostnameVerifier() {-
 @Override-
 public boolean verify(String urlHostName, SSLSession session) {-
 System.out.println("Warning: URL Host: " + urlHostName + " vs. "-
 + session.getPeerHost());-
 return true;-
 }-
 };-
-
-
 private static void trustAllHttpsCertificates() throws Exception {-
 javax.net.ssl.TrustManager\[\] trustAllCerts = new javax.net.ssl.TrustManager\[1\];-
 javax.net.ssl.TrustManager tm = new SllManager();-
 trustAllCerts\[0\] = tm;-
 javax.net.ssl.SSLContext sc = javax.net.ssl.SSLContext-
 .getInstance("SSL");-
 sc.init(null, trustAllCerts, null);-
 javax.net.ssl.HttpsURLConnection.setDefaultSSLSocketFactory(sc-
 .getSocketFactory());-
 }-
-
-
 static class SllManager implements javax.net.ssl.TrustManager,-
 javax.net.ssl.X509TrustManager {-
 @Override-
 public java.security.cert.X509Certificate\[\] getAcceptedIssuers() {-
 return null;-
 }-
-
-
 public boolean isServerTrusted(-
 java.security.cert.X509Certificate\[\] certs) {-
 return true;-
 }-
-
-
 public boolean isClientTrusted(-
 java.security.cert.X509Certificate\[\] certs) {-
 return true;-
 }-
-
-
 @Override-
 public void checkServerTrusted(-
 java.security.cert.X509Certificate\[\] certs, String authType)-
 throws java.security.cert.CertificateException {-
 return;-
 }-
-
-
 @Override-
 public void checkClientTrusted(-
 java.security.cert.X509Certificate\[\] certs, String authType)-
 throws java.security.cert.CertificateException {-
 return;-
 }-
 }-
\[/code\]-
-
-

-

本文转自 [https://www.eqishare.com/programming/95.html](https://www.eqishare.com/programming/95.html)，如有侵权，请联系删除。