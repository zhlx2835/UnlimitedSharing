最近在在弄maven项目，maven项目建好了之后，点击了disable maven nature，去掉maven的构建方式， 但是之后又想恢复maven构建方式。原来在eclipse中，在项目上右键Configure->Convert to Maven Project.就行了。 但是现在使用的是MyEclipse，在项目上右键，没有发现Configure菜单。 解决办法如下 Window > Preferences > General > Capabilities > Advanced > MyEclipse Standard Tools >WTP Deprecated(Leave off) 然后点击OK,Apply，OK就行了。再在项目上右键就有Configure菜单了，二级菜单Convert to Maven Project也有了。-

-

本文转自 [https://www.eqishare.com/programming/123.html](https://www.eqishare.com/programming/123.html)，如有侵权，请联系删除。