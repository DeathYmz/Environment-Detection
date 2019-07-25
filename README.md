# Environment-Detection
基于Zigbee的智能农业大棚环境检测（Intelligent Agricultural Greenhouse Environment Detection Based on Zigbee）

## 简介：
首先搭建一个智能农业大棚环境检测系统，然后编写传感器采集程序、协调器串口发送程序和PC机显示界面程序。能够实现环境变量的采集、显示甚至调节的功能。
通过登录，账号为数据库存在的可注册，界面显示实时数据，接受到的数据存入到数据库。并根据接收数据的情况利用链表，建立显示网络拓扑结构图。

## 环境：
开发平台： Windows java version "1.8.0_191" IAR8.10 WSN-CS源码 Sql Server2012
物理设备： ETC-WSN物联网实验平台  温湿度传感器，光敏传感器，电机，协调器，路由节点


## 使用说明：
代码模块非常多，主要分为：设备控制，环境监测，数据存储，登录验证，报错处理，历史查询，界面几个模块
关于数据库方面也就是 OutFile包中Connnet.java 里面数据库访问参数设置为自己的账号密码
数据库使用有两个表：manage(用户名(char),密码(char)),MyDate_W(温度f(loat),湿度(float),灯状态(int),烟雾(int),光强反馈(float),操作日期(datetime),其他(char),光照(int))
在使用传感器的时候要进行烧写 ，至于怎么读懂接收数据 要参考Zigbee无线传感网分析与实验手册


## 其他：
·数据库安全方面还要继续加强
·想要适用于别的物理设备，如换成软件平台则要处理收发数据这里，此处默认接收数据，并根据接收数据发出相应指令。
