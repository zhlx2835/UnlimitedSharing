\[attachment=751\]-
-
**activity\_main.xml文件代码：**-
-
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"-
 xmlns:tools="http://schemas.android.com/tools"-
 android:orientation="vertical"-
 android:layout\_width="fill\_parent"-
 android:layout\_height="fill\_parent" >-
-
 <TextView-
 android:layout\_width="fill\_parent"-
 android:layout\_height="wrap\_content"-
 android:text="@string/hello\_world"-
 tools:context=".MainActivity" />-
 <EditText-
 android:layout\_width="fill\_parent"-
 android:layout\_height="wrap\_content"-
 android:id="@+id/haoma"-
 />-
 <Button-
 android:layout\_width="wrap\_content"-
 android:layout\_height="wrap\_content"-
 android:text="@string/call"-
 android:id="@+id/call"-
 />-
</LinearLayout>-
**MainActivity.java代码：**-
-
private EditText haoma;-
 @Override-
 public void onCreate(Bundle savedInstanceState) {-
 super.onCreate(savedInstanceState);-
 setContentView(R.layout.activity\_main);-
 Button call=(Button)findViewById(R.id.call);-
 haoma=(EditText)findViewById(R.id.haoma);-
 call.setOnClickListener(new ButtonOnClickListener());-
 }-
 private final class ButtonOnClickListener implements OnClickListener{-
 @Override-
 public void onClick(View v) {-
 String str=haoma.getText().toString();-
 **Intent intent = new Intent();**-
** intent.setAction("android.intent.action.CALL");//调用android电话窗口**-
** intent.setData(Uri.parse("tel:"+ str));**-
 startActivity(intent);-
 }-
 }-
**AndroidMainfest.xml文件，设置拨打电话的权限：**-
<uses-permission android:name="android.permission.CALL\_PHONE"/>-
**例子下载：[http://dl.vmall.com/c0blir7cp3](https://www.eqishare.com/programming/473.html)**-
-
-
-

-

本文转自 [https://www.eqishare.com/programming/473.html](https://www.eqishare.com/programming/473.html)，如有侵权，请联系删除。