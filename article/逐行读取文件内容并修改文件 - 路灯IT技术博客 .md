package readFile;-
import java.io.BufferedReader;-
import java.io.BufferedWriter;-
import java.io.FileWriter;-
import java.io.FileReader;-
import java.io.IOException;-
import java.io.File;-
import java.util.\*;-
import java.lang.String;-
-
public class UpdateFile {-
-
-
public static void main(String \[\] args){-
-
 try{-
 //读取给定目录下的所有文件-
 File dir = new File("G:\\\\oldPlayer");-
 File\[\] files = dir.listFiles();-
 if (files == null)-
 return;-
 //文件名-
 String fileName = "";-
 for (int i = 0; i < files.length; i++) {-
 //判断此文件是否是一个文件-
 if (!files_.isDirectory()) {_-
 System.out.println(files_.getName());_-
 fileName = files_.getName();_-
 modifyFile(fileName);-
 }-
 }-
 }catch(Exception ex){-
 ex.printStackTrace();-
 System.out.println("file read or write error");-
 }-
}-
-
-
public static void modifyFile(String fileName) {-
 try{-
 //文件路径-
 String filePath = "";-
 //修改后新文件路径-
 String newFilePath = "";-
 filePath = "G:\\\\oldPlayer\\\\" + fileName;-
 //读取文件-
 BufferedReader File\_pwd=new BufferedReader(new FileReader(filePath));-
 //将文件内容按行存到list;-
 List<String> list=new ArrayList<String>();-
 //声明读文件行的临时变量-
 String temp;-
 do{-
 //按行循环读取文件-
 temp=File\_pwd.readLine();-
 System.out.println("读取到的原文件:"+temp);-
 list.add(temp);-
 //把读取到的行存入数组变量-
 }while(temp!=null);-
 File\_pwd.close();-
-
 //将内容写到新文件-
 newFilePath = "G:\\\\newPlayer\\\\" + fileName;-
 BufferedWriter File\_bak=new BufferedWriter(new FileWriter(new File(newFilePath)));-
 String s=new String();-
 //为注释行的标示-
 int commentFlag = 0;-
 for(int j=0;j<list.size()-1;j++){-
 //使用循环把行字符串取出来,并调用replaceall函数,对字符内容进行正则表达式替换-
 s=list.get(j);-
 if (s.indexOf("//") >= 0 || s.indexOf("\*") >= 0) {-
 s = s + " ";-
 commentFlag = 1;-
 } else if (!"".equals(s.trim())) {-
 commentFlag = 0;-
 }-
 //如果前一行为注释行，该行为空行则删除-
 if (commentFlag == 1) {-
 if (!"".equals(s.trim())) {-
 s.replace(" ", " ");-
 File\_bak.write(s+"\\n");-
 }-
 } else {-
 s.replace(" ", " ");-
 File\_bak.write(s+"\\n");-
 }-
 }-
 //必须先刷新,才能用close关闭-
 File\_bak.flush();-
 File\_bak.close();-
 System.out.println("file write success");-
 }catch(IOException ex){-
 ex.printStackTrace();-
 System.out.println("file read or write error");-
 }-
}-
}-
-
-

-

本文转自 [https://www.eqishare.com/programming/775.html](https://www.eqishare.com/programming/775.html)，如有侵权，请联系删除。