#检查一个表的id不在另一个表中-
-
#1效率最慢 142s 359607-
SELECT \* FROM saas\_gong\_yu\_student\_check WHERE sgysc\_task\_id NOT IN (SELECT sgyrw\_task\_id FROM saas\_gong\_yu\_ren\_wu );-
#2.使用左链接 202s 359607-
SELECT \* FROM saas\_gong\_yu\_student\_check LEFT JOIN saas\_gong\_yu\_ren\_wu ON sgyrw\_task\_id = sgysc\_task\_id-
WHERE sgyrw\_task\_id IS NULL;-
#3. 155s 359607-
/\*-
逻辑相对复杂,但是速度最快-
就是WHERE后查询语句，根据id查询：-
如果A中有，B中也有，就为真，返回1，得到1=0不成立，就不输出-
如果A中有，B中没有，就为假，返回0，得到0=0成立，就输出-
即可以得到A中存在而B中不存在的数据-
\*/-
SELECT \* FROM saas\_gong\_yu\_student\_check sgytc WHERE (SELECT COUNT(1) as num FROM saas\_gong\_yu\_ren\_wu sgyrw WHERE sgyrw.sgyrw\_task\_id = sgytc.sgysc\_task\_id)=0;-

-

本文转自 [https://www.eqishare.com/programming/14.html](https://www.eqishare.com/programming/14.html)，如有侵权，请联系删除。