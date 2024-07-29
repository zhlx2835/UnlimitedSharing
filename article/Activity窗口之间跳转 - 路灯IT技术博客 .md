\[attachment=795\]-
-
Activity窗口之间跳转 主要代码:-
public void onCreate(Bundle savedInstanceState) {-
 super.onCreate(savedInstanceState);-
 setContentView(R.layout.activity\_main);-
 Button button = (Button)findViewById(R.id.firstbtn);-
 button.setOnClickListener(new OnClickListener() {-
 @Override-
 public void onClick(View v) {-
 Intent intent = new Intent();-
 intent.setClass(MainActivity.this, SecondActivity.class);-
 startActivity(intent);-
 MainActivity.this.finish();-
 }-
 });-
 }-
 ----------------------------
 <activity-
 android:name=".SecondActivity"-
 android:label="@string/title\_second\_activity\_main"></activity>-
-
例子地址:-
[http://dl.vmall.com/c03xmasbbi](https://www.eqishare.com/programming/452.html)-
[http://pan.baidu.com/share/link?shareid=135319&uk=3087224563](https://www.eqishare.com/programming/452.html)-
-
-
-
-
-
-
-

-

本文转自 [https://www.eqishare.com/programming/452.html](https://www.eqishare.com/programming/452.html)，如有侵权，请联系删除。