---
layout:
title: Android Studio配置opencv
description: "Chen"
modified: 2020-11-24
tags: opencv
---   
# 步骤一  
android studio 4.1导入步骤：`File`->`New`->`import Module`,选择sdk路径：`D:\opencv-3.4.5-android-sdk\OpenCV-android-sdk\sdk\java`。  
# 步骤二  
`File`->`Project Structure`,选择`Dependencies`,为`Modules`中的`app`增加依赖项（opencv）。  
# 步骤三  
在`app/src/main`下新建`jniLibs`包，将`D:\opencv-3.4.5-android-sdk\OpenCV-android-sdk\sdk\native\libs`下的文件复制到`jniLibs`下。可能需要在`app`的`build.gradle`中增加`compile project(path: ':openCVLibrary345')`  
# 步骤四  
更改`openCVLibrary345`包下的`build.gradle`，将其中的版本改成和`app`下的`build.gradle`中版本一致。   

# Android studio 取消代理  
windows下Android studio[取消代理](https://www.jiaozn.com/reed/633.html)  

# 调用libopencv_java3.so  
主要[参考](https://blog.csdn.net/m0_37388625/article/details/104336854)，在Android studio中封装的so算法库要调用opencv时，可以使用该方法添加opencv库。需要的include头文件和so文件均在OpenCV-android-sdk中
