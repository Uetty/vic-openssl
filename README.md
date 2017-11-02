# lhtw-openssl
使用openssl api生成基于私有ca的自签名证书
resources/jni中的.cpp文件为c++调用openssl api的源码
编译后的.so文件为libs/libLhtwSSL.so
编译依赖的动态链接库也在libs/文件夹下，见.so.10文件
bcprov.jar是用于将pcks12（p12）格式的文件转为bks格式的文件使用，java编写的安卓程序只能使用bks格式文件


将c++源码编译为动态链接库需安装openssl开发版，以及jdk开发版（不是jre），jdk中需要有jni.h等c头文件，我使用eclipse编译的，编译时需指定jni.h和openssl的两个.h头文件（名字好像和动态库同名，有一段时间了，忘了）