# Cordova自动化打包
下面是一个自动打包的脚本：
请将下面的一些路径进行修改，拷贝到cordova根目录，重命名为build.sh文件，

以下是脚本内容
```
#!/bin/bash

# 这是生成正式apk的脚本文件
#   !!!!!!!!!!!!!!!!!!使用脚本前，请先修改应用的访问路径，并修改应用的版本号!!!!!!!!!!!!!!!!
#   可以按照自己的需求修改相应的路径或者是相关的配置
#   使用本脚本的前提：必须有一个cordova项目
#   cd到cordova的根目录,通过./build.sh命令运行脚本

# 按照日期生成一个apk名称
appName="$(date "+DEMO_%Y%m%d.apk")"
# 生成可以发布的release版本
cordova build android --release
# 拷贝生成的apk到根目录（这里的应用名称以及路径需要更改）
cp platforms/android/build/outputs/apk/android-armv7-release-unsigned.apk android-armv7-release.apk
# 签名文件(别名需要更改)
jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore my-release-key.keystore android-armv7-release.apk <alias_name>
# password: XXX
# 拷贝文件到桌面
cp android-armv7-release.apk ~/Desktop/$appName

```

接下来，添加运行权限
```
chmod +x build.sh
```
运行脚本
```
./build.sh
```
windows用户请在gitbash中运行脚本。

© 本文版权归作者和ETENG-WIKI所共有，转载请注明出处。
