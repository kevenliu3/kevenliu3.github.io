---
layout: post
title: FJ
date: 2018-09-23
tags: Interview
---

##### 工作职责
1. 负责android的系统以及App的开发和维护;
```java
* audioprofile：标准、静音、户外、震动
** 铃声设置：type(music ringtone alarm notification system)
*** MediaSacanner.java -- 扫码媒体文件，将结果存放com.android.providers.media/databases目录下
*** 设置下的铃声选择界面Ringtonepreference.java - RingtonePickerActivity.java 将不同情景模式下的value保存找settings_system.xml
** 音量调节
*** 捕获音量按键时间 - adjustSuggestedStreamVolume

* deskclock：时间、闹钟、秒表、倒计时
```



2. 熟悉Android 的重要Service,如ActivityManagerService,WindowManagerService,SurfaceFlinger，media等;

```java
* ActivityManagerService：主要负责系统中四大组件的启动、切换、调度及应用进程的管理和调度等工作，其职责与操作系统中的进程管理和调度模块相类似。
[AMS](http://wiki.jikexueyuan.com/project/deep-android-v2/activity.html,AMS)

* WindowManagerService：SurfaceFlinger服务在渲染整个屏幕的UI的时候，会对各个窗品的可见性进行计算，因此，WindowManagerService服务只要将它所管理的各个窗品的位置以及大小告诉SurfaceFlinger服务。
[WMS](https://blog.csdn.net/Luoshengyang/article/details/8462738,WMS)

* SurfaceFlinger:作为负责绘制应用UI的核心，从名字可以看出其功能是将所有Surface合成工作
[SF](http://gityuan.com/2017/02/05/graphic_arch/,SF)
```



3. 熟悉Android 的 App 开发，有至少一个系统App开发维护经验;

4. 加分项：对性能稳定性有深入理解和经验。
```
性能：IO/网络/内存/CPU  Android Profile
稳定性：monkey ANR crash
```



##### 任职要求

5. 本科及以上学历，具有一定的 Android 项目开发经验，工作年限不限；
6. 熟悉Android工作机制，具备扎实的JAVA编程基础；
7. 熟悉Android应用开发，如熟悉系统控件、动画、多线程、网络协议、数据库、XML/JSON解析等；

```java
* TextView类：文本框
* Button类：按钮
* EditText类：编辑框
* DatePicker类：日期选择
* TimePicker类：时间选择
* ProgressBar类：进度条
* SeekBar类：滑块
* RatingBar类：星级滑块
* ToggleButton类：状态开关按钮
* Toast类：弹出信息框
* CheckBox类：复选框
* RadioButton类和RadioGroup类：单选框
* ImageView类：图片
* Spinner类：下拉列表
* AutoCompleteTextView类：自动完成文本框
* Gallery类：画廊
* ListView：列表
[系统控件](http://www.dwenzhao.cn/profession/handhold/androidtextview.html,SW)
```



5. 代码风格良好，能设计出高效合理，易读易拓展的程序结构；

```java
[设计模式](https://www.jianshu.com/p/1a9f571ad7c0，SJMS)
[APP架构](https://blog.csdn.net/ganyao939543405/article/details/52594395,APPS)
```



5. 加分项：具备Kotlin /C/C++ 相关经验，或者在OpenGL、视频图像处理、编解码方面有相关经验。

```java
* C/C++:JNI
* kotlin：
* OpenGL：opencv（图像采集 - 图像去干扰 - 图像特征值 - 图像匹配）
```

