有时候怎么也连不上，提交不了。可以试试这个。

》》git设置代理 -github设置代理

git config --global http.proxy "127.0.0.1:10802"

git config --global https.proxy \[http://127.0.0.1:1080\](http://127.0.0.1:1080/)

》》git取消代理-github取消代理

git config --global --unset http.proxy

git config --global --unset https.proxy

-

-

本文转自 [https://www.eqishare.com/programming/918.html](https://www.eqishare.com/programming/918.html)，如有侵权，请联系删除。