import java.io.\*;-
import org.apache.tools.zip.ZipOutputStream;-
import org.apache.tools.zip.ZipEntry;-
public class demo1 {-
 public static void main( String\[\] args ) {-
 try {-
 String\[\] strs = new String\[5\];-
 strs\[0\]="D:/workspace\_myeclipse/GZRAIL/src/www/resource/word/lessonmanager/doc1/钟如燕.doc";-
 strs\[1\]="D:/workspace\_myeclipse/GZRAIL/src/www/resource/word/lessonmanager/doc1/马蓉.doc";-
 strs\[2\]="D:/workspace\_myeclipse/GZRAIL/src/www/resource/word/lessonmanager/doc1/邹青宜.doc";-
 strs\[3\]="D:/workspace\_myeclipse/GZRAIL/src/www/resource/word/lessonmanager/doc1/周黎.doc";-
 strs\[4\]="D:/workspace\_myeclipse/GZRAIL/src/www/resource/word/lessonmanager/doc1/邝莉莉.doc";-
 //文件的列表 和 将要打成的zip文件的名称-
 writeZip(strs,"123456");-
 } catch ( IOException e ) {-
 e.printStackTrace();-
 }-
 }-
 private static void writeZip(String\[\] strs,String zipname) throws IOException {-
 String\[\] files = strs;-
 OutputStream os = new BufferedOutputStream( new FileOutputStream( "D:/workspace\_myeclipse/GZRAIL/src/www/resource/word/lessonmanager/doc1/"+zipname+".zip" ) );-
 ZipOutputStream zos = new ZipOutputStream( os );-
 byte\[\] buf = new byte\[8192\];-
 int len;-
 for (int i=0;i<files.length;i++) {-
 File file = new File( files );-
 if ( !file.isFile() ) continue;-
 ZipEntry ze = new ZipEntry( file.getName() );-
 zos.putNextEntry( ze );-
 BufferedInputStream bis = new BufferedInputStream( new FileInputStream( file ) );-
 while ( ( len = bis.read( buf ) ) > 0 ) {-
 zos.write( buf, 0, len );-
 }-
 zos.closeEntry();-
 }-
 zos.setEncoding("GBK");-
 zos.closeEntry();-
 zos.close();-
-
 for(int i=0;i<files.length;i++){-
 System.out.println("------------"+files );-
 File file= new File(files );-
 file.delete();-
 }-
 }-
}-
jar包下载：\[attachment=501\]-
-

-

本文转自 [https://www.eqishare.com/programming/572.html](https://www.eqishare.com/programming/572.html)，如有侵权，请联系删除。