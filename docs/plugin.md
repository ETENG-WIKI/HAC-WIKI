# Cordova插件
- 什么是Cordova插件？  
cordova插件是APP用来调用系统硬件应用的一种途径，可以进行拍照，扫码等一系列操作。

- 为什么使用Cordova插件？  
如果不使用Cordova插件，打包出的应用就是一个网页，用户只能进行浏览操作，用户体验会大打折扣。

- Cordova插件原理  
js通过调用原生代码（例如：android）,来实现对于原生硬件的调用:  
```
//调用接口示例：使用cordova.exec实现js的接口
exec(<successFunction>, <failFunction>, <service>, <action>, [<args>]);
```
>具体的插件制作，请参看官方文档

- 插件的添加和移除  
```
//插件添加,--save代表保存这个插件到配置文件
cordova plugin rm <plugin-name> --save
//插件删除
cordova plugin rm <plugin-name>
```

- Cordova常用插件
    * cordova-plugin-splashscreen 闪屏插件
    * cordova-plugin-file-transfer 文件传送
    * cordova-plugin-whitelist 白名单
    * cordova-open 打开文件
    * cordova-plugin-app-version 获取应用信息
    * cordova-plugin-camera 拍照插件
    * phonegap-plugin-barcodescanner 二维码插件
    * cordova-plugin-wechat 微信分享插件

© 本文版权归作者和ETENG-WIKI所共有，转载请注明出处。
