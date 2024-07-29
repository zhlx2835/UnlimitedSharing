**JSONArray:\["100","102","false"\]**-
**JSONArray中放入JSONObject:\[{"0":100},{"1":101},{"2":102},{"3":103},{"4":104}\]**-
**JSONObject:{"2":329,"1":"str"}**-
**多个JSONObject:{"1":{"3":"河东","2":"河北","1":"河南"},"0":{"3":"河东","2":"河北","1":"河南"}}**-
代码：-
public static void main(String\[\] args) {-
 //-------------JSONArray-
 JSONArray ja = new JSONArray();-
 ja.add("100");-
 ja.add("102");-
 ja.add("false");-
 System.out.println(ja.toJSONString());-
 //-------------JSONArray中放入JSONObject-
 JSONArray jsonArray = new JSONArray();-
 for(int i=0;i<5;i++){-
 Map map1 = new HashMap();-
 map1.put(i,i+100);-
 JSONObject jo1=new JSONObject(map1);-
 jsonArray.add(jo1);-
 }-
 System.out.println(jsonArray.toJSONString());-
 //-------------JSONObject-
 Map map = new HashMap();-
 map.put("1","str");-
 map.put("2",329);-
 JSONObject jo = new JSONObject(map);-
 System.out.println(jo.toJSONString());-
 //-------------多个JSONObject-
 JSONObject jo2 = new JSONObject();-
 for(int i=0;i<2;i++){-
 Map map1 = new HashMap();-
 map1.put("1","河南");-
 map1.put("2","河北");-
 map1.put("3","河东");-
 jo2.put(i,map1);-
 }-
 System.out.println(jo2.toJSONString());-
}-

-

本文转自 [https://www.eqishare.com/programming/538.html](https://www.eqishare.com/programming/538.html)，如有侵权，请联系删除。