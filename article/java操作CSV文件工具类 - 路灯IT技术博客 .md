这里写一写用java怎么读取excel中csv格式的文件。下面是一个例子。-
-
//JAVA 操作 excel 中的 .csv文件格式-
public class CsvUtil {-
 private String filename = null;-
 private BufferedReader bufferedreader = null;-
 private List list =new ArrayList();-
 public CsvUtil() { }-
-
 public CsvUtil(String filename) throws IOException{-
 this.filename = filename;-
 bufferedreader = new BufferedReader(new FileReader(filename));-
 String stemp;-
 while((stemp = bufferedreader.readLine()) != null){-
 list.add(stemp);-
 }-
 }-
-
 public List getList() throws IOException {-
 return list;-
 }-
//得到csv文件的行数-
 public int getRowNum(){-
 return list.size();-
 }-
 //得到csv文件的列数-
 public int getColNum(){-
 if(!list.toString().equals("\[\]")) {-
 if(list.get(0).toString().contains(",")) { //csv文件中，每列之间的是用','来分隔的-
 return list.get(0).toString().split(",").length;-
 }else if(list.get(0).toString().trim().length() != 0) {-
 return 1;-
 }else{-
 return 0;-
 }-
 }else{-
 return 0;-
 }-
 }-
-
//取得指定行的值-
public String getRow(int index) {-
 if (this.list.size() != 0)-
 return (String) list.get(index);-
 else-
 return null;-
 }-
 //取得指定列的值-
 public String getCol(int index){-
 if (this.getColNum() == 0){-
 return null;-
 }-
 StringBuffer scol = new StringBuffer();-
 String temp = null;-
 int colnum = this.getColNum();-
 if (colnum > 1){-
 for (Iterator it = list.iterator(); it.hasNext();) {-
 temp = it.next().toString();-
 scol = scol.append(temp.split(",")\[index\] + ",");-
 }-
 }else{-
 for (Iterator it = list.iterator(); it.hasNext();) {-
 temp = it.next().toString();-
 scol = scol.append(temp + ",");-
 }-
 }-
 String str=new String(scol.toString());-
 str = str.substring(0, str.length() - 1);-
 return str;-
 }-
 //取得指定行，指定列的值-
 public String getString(int row, int col) {-
 String temp = null;-
 int colnum = this.getColNum();-
 if(colnum > 1){-
 temp = list.get(row).toString().split(",")\[col\];-
 }else if(colnum == 1) {-
 temp = list.get(row).toString();-
 }else{-
 temp = null;-
 }-
 return temp;-
 }-
-
 public void CsvClose() throws IOException {-
 this.bufferedreader.close();-
 }-
-
 public void run(String filename) throws IOException {-
 CsvUtil cu = new CsvUtil(filename);-
 for(int i=0;i<cu.getRowNum();i++){-
-
 String name = cu.getString(i,0);//得到第i行.第一列的数据.-
 String email = cu.getString(i,1);//得到第i行.第二列的数据.-
 String tel = cu.getString(i,2);-
 String number = cu.getString(i,3);-
-
 System.out.println("===name:"+name);-
 System.out.println("===email:"+email);-
 System.out.println("===tel:"+tel);-
 System.out.println("===number:"+number);-
 System.out.println(" ");-
 }-
 cu.CsvClose();-
 }-
 public static void main(String\[\] args) throws IOException {-
 CsvUtil test = new CsvUtil();-
 test.run("D:/alpha/abc.csv");-
 }-
}-
-
-
-
例子2-
\=================================================================================-
public class CsvUtil1 {-
private String filename = null;-
private BufferedReader bufferedreader = null;-
private List list = new ArrayList();-
public CsvUtil1() {-
}-
public CsvUtil1(String filename) throws IOException {-
this.filename = filename;-
bufferedreader = new BufferedReader(new FileReader(filename));-
String stemp;-
while ((stemp = bufferedreader.readLine()) != null) {-
list.add(stemp);-
}-
}-
public List getList() throws IOException {-
return list;-
}-
public int getRowNum() {-
return list.size();-
}-
public int getColNum() {-
if (!list.toString().equals("\[\]")) {-
if (list.get(0).toString().contains(",")) {-
return list.get(0).toString().split(",").length;-
} else if (list.get(0).toString().trim().length() != 0) {-
return 1;-
} else {-
return 0;-
}-
} else {-
return 0;-
}-
}-
public String getRow(int index) {-
if (this.list.size() != 0)-
return (String) list.get(index);-
else-
return null;-
}-
public String getCol(int index) {-
if (this.getColNum() == 0) {-
return null;-
}-
StringBuffer scol = new StringBuffer();-
String temp = null;-
int colnum = this.getColNum();-
if (colnum > 1) {-
for (Iterator it = list.iterator(); it.hasNext();) {-
temp = it.next().toString();-
scol = scol.append(temp.split(",")\[index\] + ",");-
}-
} else {-
for (Iterator it = list.iterator(); it.hasNext();) {-
temp = it.next().toString();-
scol = scol.append(temp + ",");-
}-
}-
String str = new String(scol.toString());-
str = str.substring(0, str.length() - 1);-
return str;-
}-
public String getString(int row, int col) {-
String temp = null;-
int colnum = this.getColNum();-
if (colnum > 1) {-
temp = list.get(row).toString().split(",")\[col\];-
} else if (colnum == 1) {-
temp = list.get(row).toString();-
} else {-
temp = null;-
}-
return temp;-
}-
public void CsvClose() throws IOException {-
this.bufferedreader.close();-
}-
public void test() throws IOException {-
CsvUtil1 cu = new CsvUtil1("D:/学习/00dw.csv");-
List tt = cu.getList();-
for (Iterator itt = tt.iterator(); itt.hasNext();) {-
System.out.println(itt.next().toString()+"||");-
}-
// System.out.println(cu.getRowNum());-
// System.out.println(cu.getColNum());-
// System.out.println(cu.getRow(0));-
// System.out.println(cu.getCol(0));-
// System.out.println(cu.getString(0, 0));-
cu.CsvClose();-
}-
public void createCsvTest1(HttpServletResponse Response) throws IOException {-
CsvUtil1 cu = new CsvUtil1("D:/学习/00dw.csv");-
List tt = cu.getList();-
String data = "";-
-
SimpleDateFormat dataFormat = new SimpleDateFormat("yyyyMMddHHmm");-
Date today = new Date();-
String dateToday = dataFormat.format(today);-
File file=new File("D:/学习/001dw.csv");-
if(!file.exists())-
file.createNewFile();-
// else-
// file.delete() ;-
String str\[\] ;-
StringBuilder sb = new StringBuilder("");-
BufferedWriter output=new BufferedWriter(new FileWriter(file,true));-
for (Iterator itt = tt.iterator(); itt.hasNext();) {-
String fileStr = itt.next().toString() ;-
str = fileStr.split(",");-
for(int i=0;i<=str.length-1;i++){ //拆分成数组 用于插入数据库中-
System.out.print("str\["+i+"\]="+str_+" ");-
}-
System.out.println("");-
sb.append(fileStr+"\\r\\n") ;-
}-
//System.out.println(sb.toString());-
output.write(sb.toString());-
output.flush() ;-
output.close();-
cu.CsvClose();-
}-
public static void main(String\[\] args) throws IOException {-
CsvUtil1 test = new CsvUtil1();-
//test.test();-
HttpServletResponse response = null ;-
test.createCsvTest1(response);-
}-
}-
-
-
下面是另一个材料-
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*-
public static String readExcel(){-
 StringBuffer sb = new StringBuffer();-
 File file = new File("D:\\\\test.xls");-
 Workbook wb = null;-
 try {-
// 构造Workbook（工作薄）对象-
 wb = Workbook.getWorkbook(file);-
 //获得了Workbook对象之后，就可以通过它得到Sheet（工作表）对象了-
 Sheet\[\] sheet = wb.getSheets();-
 if(sheet!=null&&sheet.length>0){-
 //对每个工作表进行循环-
 System.out.println("sheet.length="+sheet.length);-
 for(int i=0;i<sheet.length;i++){-
 int rowNum = sheet_.getRows();-
 System.out.println("rowNum="+rowNum);-
 for(int j=0;j<rowNum;j++){-
// 得到当前行的所有单元格-
 Cell\[\] cells = sheet_.getRow(j);-
 System.out.println("cells.length="+cells.length);-
 if(cells!=null&&cells.length>0){-
// 对每个单元格进行循环-
 for(int k=0;k<cells.length;k++){-
 //读取当前单元格的值-
 String cellValue = cells\[k\].getContents();-
 sb.append(cellValue+"\\t");-
 }-
 }-
 sb.append("\\r\\n");-
 }-
 sb.append("\\r\\n");-
 }-
 }-
 } catch (BiffException e) {-
 e.printStackTrace();-
 } catch (IOException e) {-
 e.printStackTrace();-
 }-
 System.out.println(sb.toString());-
// 最后关闭资源，释放内存-
 wb.close();-
 return sb.toString();-
}-
-
___

-

本文转自 [https://www.eqishare.com/programming/657.html](https://www.eqishare.com/programming/657.html)，如有侵权，请联系删除。