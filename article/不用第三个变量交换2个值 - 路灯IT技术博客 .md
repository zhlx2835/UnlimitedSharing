面试的时候遇到过这样的问题。-
**不借助第三个变量让2个变量交换值。**-
-
-
public static void main(String\[\] args) {-
 int a = 10;-
 int b = 12;-
 a = b + (b = a) \* 0; // 这句实现交换-
 System.out.println("a:" + a + " b:" + b);-
}-
-
-
对于这段代码片段：-
**int** a = 1;-
**int** b = 2;-
a = b + (b = a) \* 0;-
如果将其转换为静态单赋值形式，并限制每个语句都是一个二元运算与一个赋值，就变成：-
int a0 = 1;-
int b0 = 2;-
int b1 = a; // (b = a)-
int temp1 = b1 \* 0; // (b = a) \* 0-
int a1 = b0 + temp1; // b + (b = a) \* 0-
这样就比较明显了：a0、b0是交换前的值，a1、b1是交换后的值。-
说真的这样写只是在自己的代码里少用了个临时变量而已。编译器还是得插入一些临时变量，并不是说自己少用了显式的变量就等于实际运行效率高。-

-

本文转自 [https://www.eqishare.com/programming/652.html](https://www.eqishare.com/programming/652.html)，如有侵权，请联系删除。