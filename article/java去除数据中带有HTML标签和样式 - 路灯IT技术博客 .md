-
/\*\*-
 \* 清除Html标签-
 \*-
 \* @param inputString 目标字符串-
 \* @return 处理后的结果-
 \*/-
 public static String removeHtmlTag(String inputString) {-
 if (inputString == null)-
 return null;-
 String htmlStr = inputString; // 含html标签的字符串-
 String textStr = "";-
 Pattern p\_script;-
 Matcher m\_script;-
 Pattern p\_style;-
 Matcher m\_style;-
 Pattern p\_html;-
 Matcher m\_html;-
 Pattern p\_special;-
 Matcher m\_special;-
 try {-
 //定义script的正则表达式{或<script\[^>\]\*?>\[\\\\s\\\\S\]\*?<\\\\/script>-
 String regEx\_script = "<\[\\\\s\]\*?script\[^>\]\*?>\[\\\\s\\\\S\]\*?<\[\\\\s\]\*?\\\\/\[\\\\s\]\*?script\[\\\\s\]\*?>";-
 //定义style的正则表达式{或<style\[^>\]\*?>\[\\\\s\\\\S\]\*?<\\\\/style>-
 String regEx\_style = "<\[\\\\s\]\*?style\[^>\]\*?>\[\\\\s\\\\S\]\*?<\[\\\\s\]\*?\\\\/\[\\\\s\]\*?style\[\\\\s\]\*?>";-
 // 定义HTML标签的正则表达式-
 String regEx\_html = "<\[^>\]+>";-
 // 定义一些特殊字符的正则表达式 如：-
 String regEx\_special = "\\\\&\[a-zA-Z\]{1,10};";-
-
 p\_script = Pattern.compile(regEx\_script, Pattern.CASE\_INSENSITIVE);-
 m\_script = p\_script.matcher(htmlStr);-
 htmlStr = m\_script.replaceAll(""); // 过滤script标签-
 p\_style = Pattern.compile(regEx\_style, Pattern.CASE\_INSENSITIVE);-
 m\_style = p\_style.matcher(htmlStr);-
 htmlStr = m\_style.replaceAll(""); // 过滤style标签-
 p\_html = Pattern.compile(regEx\_html, Pattern.CASE\_INSENSITIVE);-
 m\_html = p\_html.matcher(htmlStr);-
 htmlStr = m\_html.replaceAll(""); // 过滤html标签-
 p\_special = Pattern.compile(regEx\_special, Pattern.CASE\_INSENSITIVE);-
 m\_special = p\_special.matcher(htmlStr);-
 htmlStr = m\_special.replaceAll(""); // 过滤特殊标签-
 textStr = htmlStr;-
 } catch (Exception e) {-
 e.printStackTrace();-
 }-
 return textStr;// 返回文本字符串-
 }

-

本文转自 [https://www.eqishare.com/programming/79.html](https://www.eqishare.com/programming/79.html)，如有侵权，请联系删除。