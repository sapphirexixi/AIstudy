# Day 1


```
1.装Ubuntu22.04，____虚拟机版
2.复习使用GitHub
3.装ROS2，____humble
4.仔细浏览了sim2real和无人机竞赛官网，但是发现好像并不能参加？至少这个时间点是不能报名参赛的
目前方向一直是导航 _定位感觉可以做一做
5.洗澡了
6.复习c++使用
7.粗略掌握markdown语法
```
Git尚硅谷教学：[https://www.bilibili.com/video/BV1wm4y1z7Dg/]
# Day 2

```
1.学习Linux和shell的相关命令行
2.扩展使用markdown语法，上传GitHub学习记录
3.复习巩固C++使用
4.初步了解protobuf和yaml的相关知识
```
##### Note
###### Linux & shell：linux是操作系统内核，shell是外壳，用户通过shell外壳来控制操作系统
%%在用户用键盘和鼠标输入后，终端（Terminal）将这些输入发送给你选用的壳层（Shell），Shell解析你的命令发送给操作系统内核去执行，并把执行结果返回给终端，终端调用图形接口将结果显示到屏幕上。%%
###### Linux文件管理%%
- **/boot**：存放着启动Linux时使用的内核文件，包括连接文件以及镜像文件。
- **/etc**：存放所有的系统需要的配置文件和子目录列表。
- **/lib**：存放基本代码库（比如c++库），几乎所有的应用程序都需要用到这些共享库。
- **/sys**：该目录下安装了Linux2.6内核中新出现的一个文件系统 sysfs ，当一个内核对象被创建的时候，对应的文件和目录也在内核对象子系统中。
- **/bin**：存放着最常用的程序和指令。
- **/sbin**：只有系统管理员能使用的程序和指令。
- **/dev**：Device的缩写，存放的是Linux的外部设备。注意：在Linux中访问设备和访问文件的方式是相同的。
- **/media**：类windows的其他设备，例如U盘、光驱等等，识别后linux会把设备放到这个目录下。
- **/mnt**：用于临时挂载别的文件系统，在讲docker时可能还会遇到。
- **/run**：是一个临时文件系统，存储系统启动以来的信息。
- **/lost+found**：一般情况下为空的，系统非法关机后，这里就存放一些文件。
- **/tmp**：这个目录是用来存放一些临时文件的。
- **/root**：系统管理员的用户主目录。
- **/home**：用户的主目录，以用户的账号命名。
- **/usr**：用户的很多应用程序和文件都放在这个目录下，类似于Windows下的program files目录。
- **/usr/bin**：系统用户使用的应用程序与指令。
- **/usr/sbin**：超级用户使用的比较高级的管理程序和系统守护程序。
- **/usr/src**：内核源代码默认的放置目录。
- **/var**：存放经常修改的数据，比如程序运行的日志文件（/var/log 目录下）。
- **/proc**：管理内存空间。虚拟的目录，是系统内存的映射，我们可以直接访问这个目录来获取系统信息。这个目录的内容不在硬盘上而是在内存里，我们也可以直接修改里面的某些文件来做修改。%%

###### Shell命令符
ls：列出当前目录文件
cd：进入目录
pwd：打印当前路径
~：主目录
cp：复制
mv：移动
rm：删除
clear：清屏
cat：显示文件内容
less：少量显示（空格翻页
grep：搜索文件内容
>例：grep xxx file4（搜索file4中含xxx的每一行

wc：字数统计
>例：wc -w file4
>        wc -l file4

|命令|意义|
|---|---|
|cp file1 file2|复制file1并命名为file2|
|cp file1 xxx|复制file1至xxx目录|
|mv file xxx|把file移动到xxx目录|
|mv file1 file6|把file1重命名为file6|
|rm file|删除文件|
|cat file|在屏幕上显示文件内容|
|less file|在屏幕上显示文件部分内容|
|head file|显示文件前10行内容|
|tail file|显示文件末10行内容|
|grep xxx file|打印file中包含xxx的行|
|wc -w file|显示字数|
|wc -l file|显示行数|
|clear|清屏|

通配符\*：任意个
？：一个
###### 其他知识

chmod ()
只有文件的所有者可以使用 chmod 更改权限。chmod的选项如下

|选项|意义|
|---|---|
|u|user|
|g|group|
|o|其他|
|a|all|
|r|读|
|w|写入（和删除）|
|x|执行（和访问目录）|
|+|添加权限|
|-|取消权限|

例如，要给某文件添加执行权限，键入

```
chmod +x file
```

ctrl+C     取消进程

新建文本文档：gedit 新建文本文档.txt


Linux软链接和硬链接[[Linux软连接和硬链接 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/67366919)]
管道：管道符    |
```
[command1] | [command2] | [command3] ...
```
将多个命令连接到一起，上一个命令正确输出后执行下一个命令

env # 查看全部全局变量
printenv HOME # 查看个别全局变量（HOME）
echo $HOME # 查看个别全局变量（HOME）
- HOME ：当前用户的主目录
- PATH ： shell 查找命令的目录列表，由冒号分隔
- PWD ：当前工作目录

加载环境变量的文件
/etc/profile # 系统级，登录shell当中加载
/etc/bashrc # 系统级，可认为都会被加载
~/.profile # 用户级，登录shell当中加载
~/.bashrc # 用户级，可认为都会被加载

SSH相关知识[【科普】SSH都不懂，还搞什么网络 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/323322650)
###### C++[http://t.csdn.cn/OBhf9]
头文件header guard：#pragma once【防止重定义

