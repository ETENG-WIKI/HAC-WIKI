# Cordova入门
## 一 Cordova是什么？
Cordova，旧名为phonegap，是一个流行的手机应用开发框架。
Cordova提供了js和原生API的调用接口，通过插件，我们可以实现例如拍照，扫码等操作；
并且提供了静态文件转换成APP的功能。

## 二 为什么使用Cordova？

现在我们要开发一个APP项目，有这么几种方式：  
1. 采用原生应用  
  优点：响应速度快，用户体验较好  
  缺点：开发速度慢，成本较高  
2. 采用html5应用  
  优点：开发速度快，代码可以复用到iOS和android  
  缺点：响应速度较慢（已有很大的改善）  

cordova提供了打包html5的功能，而cordova属于apache开源基金会，可以保证较大的社区以及长期稳定的维护。

## 三 GET START
1. 首先请参考环境配置部分，然后新建一个Cordova项目  
  ```
  cordova create 项目名 <包名>
  ```
2. 添加一个平台（拿android举例）  
  ```
  cordova platform add android
  ```
3. cordova项目准备  
  ```
  cordova platform prepare
  ```
4. 打包一个测试的项目  
  ```
  cordova build
  ```
5. 安装APK，在platforms/android/build/outputs/apk下可以找到打包出来的apk，安装到手机即可。  

© 本文版权归作者和ETENG-WIKI所共有，转载请注明出处。
