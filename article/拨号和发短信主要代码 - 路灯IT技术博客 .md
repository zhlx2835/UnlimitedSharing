-
**打电话**主要代码-
Activity类：-
public void onClick(View v) {-
 String str=haoma.getText().toString();-
 Intent intent = new Intent();-
 **intent.setAction("android.intent.action.CALL");-
 intent.setData(Uri.parse("tel:"+ str));**-
 startActivity(intent);-
 }-
权限：-
<uses-permission android:name="**android.permission.CALL\_PHONE**"/>-
\---------------------------------------------------------------------------------------------------------------------
**发短信**主要代码：-
Activity类：-
-
public void onClick(View v) {-
 String number = numberText.getText().toString();-
 String content = contentText.getText().toString();-
 SmsManager manager=SmsManager.getDefault();-
 ArrayList<String> texts=manager.divideMessage(content);-
 for (String texe:texts) {-
 **manager.sendTextMessage(number, null, content, null, null);**-
 }-
 Toast.makeText(MainActivity.this, R.string.success, Toast.LENGTH\_SHORT).show();-
 }-
-
权限：-
<uses-permission android:name="**android.permission.SEND\_SMS**"/>-

-

本文转自 [https://www.eqishare.com/programming/449.html](https://www.eqishare.com/programming/449.html)，如有侵权，请联系删除。