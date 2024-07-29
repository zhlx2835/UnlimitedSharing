1 先找到指定的开始提交id，比如 05104e3475f63e1e49fbfcbd424a4a3801b95645-
2 找到结束的提交id，比如 a0eb9bc6d4e1801062877fd435eefb81f11598b8-
3 在命令行下进入到git代码目录中，敲命令制作增量包-
 git archive -o hot-fix-20151001.zip HEAD $(git diff 05104e3...a0eb9bc --name-only)-
 注：git diff 后边的commit id, 可以只取前7位或全部写上都可以-
3 命令执行完成后，在当前目录生成一个.zip的文件，这个就是增量包文件了-
Tips: 其实还可以把zip文件生成到指定目录中，把上边git archive的命令改一下-
 git archive -o /root/hot-fix-20151001.zip HEAD $(git diff 05104e3...a0eb9bc --name-only)-
-
-
例如：-
git archive -o hot-fix-20170920.zip HEAD $(git diff 10183dcacfdbaead7f8ae3efe69df6ee9ad9c06a...96b653ded1b620935f639b8f1a0ee2d368fbd329 --name-only)-
\[attachment=1490\]-
有个问题，打出的包，是java代码，没法编译。-
-
-
-
-
-
-
-
-

-

本文转自 [https://www.eqishare.com/programming/111.html](https://www.eqishare.com/programming/111.html)，如有侵权，请联系删除。