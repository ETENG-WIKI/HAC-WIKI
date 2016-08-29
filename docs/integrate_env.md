## 一 前期准备
服务器x1
docker环境x1
jekins容器x1

## 二 搭建环境
首先，远程连接服务器，准备材料，下载docker镜像。
```
docker pull yitengshidai/cordova-grunt
```
接下来，运行docker镜像，并生成可以在后台允许的容器。
```
docker run --name cordova -it -d yitengshidai/cordova-grunt bash
```
最后，进入新建的cordova容器
```
docker exec -it cordova bash
```