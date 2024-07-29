所有component的子类都自动的参与标准的ext组件的生命周期：创建，渲染，销毁，这些操作由Container类提供。在创建容器时，组件可以通过item配置选项添加到容器中，或者可以add方法动态地添加。所有组件都注册到了ext.componentMgr类，所以他可以在任何时刻通过传递Id使用EXT.getCmp方法获得引用。所以组件创建后要特别注意是不是要在没用的时候销毁，如果组件在该销毁的时候而未被销毁那么就会导致内存的泄露！

-

本文转自 [https://www.eqishare.com/programming/833.html](https://www.eqishare.com/programming/833.html)，如有侵权，请联系删除。