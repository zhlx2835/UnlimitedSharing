-
1\. Ext.Msg.alert("角色管理信息提示", "角色权限保存成功！");-
2\. store.baseParams.jsonString = jsonData;-
3\. xmlRequestForUserInfo.open('POST', 'bzRulesAction.do?method=findBzRulesByTypeNameForCount&typeName='+encodeURI(typeName),false);-
4\. window.location.reload();-
5.disabled:true, //文本框灰掉-
6.var bzEditorDoc\_value ='${offical.bzEditorDoc }';-
//下拉框赋值-
 Ext.getCmp("organCombo").setValue({id:'0',text:bzEditorDoc\_value});-
//form赋值-
Ext.getCmp("creDate").setValue(msgcredate);-
7.new window.parent.Ext.Window 的属性jsp加载不到 closeAction : 'close',当close时item中的form加载不到-
8.align :'center',居中(Ext.grid.ColumnModel中)-
9.-
new Ext.grid.EditorGridPanel的属性-
viewConfig : {-
 forceFit : true//让grid的列自动填满grid的整个宽度，不用一列一列的设定宽度。-
},-
10.window.parent.Ext.MessageBox.confirm('信息提示', '你确定提交标准吗?', function btn(btn){-
 if(btn=="yes"){}-
});-
11.encodeURI(url);

-

本文转自 [https://www.eqishare.com/programming/842.html](https://www.eqishare.com/programming/842.html)，如有侵权，请联系删除。