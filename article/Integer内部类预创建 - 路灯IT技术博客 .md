-
**这道题你肯定答错，下面代码输出什么？**-
**public static void main(String\[\] args) {**-
 **Integer a = 100;**-
 **Integer b = 100;**-
 **if (a == b) {**-
 **System.out.println("true");**-
 **} else {**-
 **System.out.println("false");**-
 **}**-
 **Integer c = 130;**-
 **Integer d = 130;**-
 **if (c == d) {**-
 **System.out.println("true");**-
 **} else {**-
 **System.out.println("false");**-
 **}**-
**}**-
-
**\-------------------------**-
**false**-
**false**-
**恭喜你答错了。**-
**\-------------------------**-
**true**-
**true**-
**再次恭喜你答错了。**-
**\-------------------------**-
**-
**-
**正确答案：**-
**true**-
**false**-
**Integer类的内部, 有一个常量静态数组, 在Integer类被加载的时候, 预先创建了-128 ~ 127的Integer对象,所以当声明的Integer类型变量的值在-128 ~ 127的范围内时, 不会新创建对象, 直接引用数组中创建好的. 所以第一个结果会输出true**

-

本文转自 [https://www.eqishare.com/programming/698.html](https://www.eqishare.com/programming/698.html)，如有侵权，请联系删除。