# Cordova配置文件
1. 文件位置
cordova配置文件位于项目根目录下的config.xml文件。

2. 配置哪些？
  >* APP名称
  >* APP包名
  >* APP版本
  >* APP闪屏以及图标
  >* APP的index网页路径
  >* 允许的网址
  >* 允许的协议
  >* 对应平台（iOS和Android）的相关配置
  >* cordova插件以及版本
  >* 其他请参考cordova官方文档，

3. 如何配置？
>* 配置APP名称  
```
<name>APP名称</name>
```
  >>* 配置APP包名
  在weget标签中，修改属性项id，例如：
```
id="com.eteng.XXX"
```
  >>* APP版本
  在weget标签中，修改属性项version，例如：
```
version="0.0.1"
```
  >>* APP闪屏以及图标（需配置相对项目根目录的相关图片路径）  
  闪屏配置  
```
<splash src="www/images/splash.png" />
```  
  icon配置  
```
<icon src="www/images/icon.png" />
```
  >>* APP的index网页路径  
```
<content src="index.html" />
```
  >>* 允许的域名  
```
//*代表所有的域名
<access origin="*" />
```
  >>* 允许的协议  
```

<allow-intent href="http://*/*" />
<allow-intent href="https://*/*" />
<allow-intent href="tel:*" />
<allow-intent href="sms:*" />
<allow-intent href="mailto:*" />
<allow-intent href="geo:*" />

```
  >>* 对应平台（iOS和Android）的相关配置  
```

//Android平台（这里是我的配置，仅供参考）
<platform name="android">
      <allow-intent href="market:*" />
      <preference name="SplashScreen" value="screen" />
      <preference name="SplashScreenDelay" value="10000" />
      <preference name="android-windowSoftInputMode" value="adjustPan|stateAlwaysHidden" />
      <preference name="Fullscreen" value="false" />
      <preference name="KeyboardDisplayRequiresUserAction" value="true" />
      <preference name="KeepRunning" value="false" />
  </platform>

```
  >>* cordova插件以及版本  
```
//一种是插件名称＋插件版本（在cordova插件平台注册插件）
<plugin name="cordova-plugin-camera" spec="~2.2.0" />
//另一种是插件名称＋插件地址（一般是自己写的插件）
<plugin name="phonegap-plugin-barcodescanner" spec="https://github.com/JrontEnd/phonegap-plugin-barcodescanner" />

```

© 本文版权归作者和ETENG-WIKI所共有，转载请注明出处。
