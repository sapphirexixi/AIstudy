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
#### Note
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



# Day 3
~~洗澡了~~
```
1.了解编译、链接、静态库、动态库相关概念
2.学习Cmake
```
#### Note
##### Ubuntu突然连不上网：解决方案
命令行输sudo vi /etc/NetworkManager/NetworkManager.conf
将其中的managed=false改为manafed=true.
修改文件时，用delete键删除false，再按 i 键进入编辑模式，编辑好后，Esc推出编辑，Shift+冒号，光标定位到最下面，输入wq(退出并保存），再回车就行。
然后再重启网络，输入：
sudo service network-manager restart
##### 编译、链接、静态库、动态库
###### 1.前言[​](https://tars-cat.github.io/docs/gcc_g++#1%E5%89%8D%E8%A8%80 "Direct link to heading")

在课堂中，我们运行一个C++程序的步骤通常是这样的：在文件中写好程序，然后点击“调试”或者“执行(不调试)”，一个黑色的方框就会弹出来。

实际上，从C++源代码文件到可执行文件的过程是十分复杂的，Visual Studio等现代化的IDE（Integrated Development Environment，集成开发环境）掩盖了程序构建的复杂流程。本节我们就以Linux平台上的C++程序为例，简略介绍C++工程中的一些概念。

###### 2.从.cpp到.exe —— C/C++程序的构建过程[​](https://tars-cat.github.io/docs/gcc_g++#2%E4%BB%8Ecpp%E5%88%B0exe--cc%E7%A8%8B%E5%BA%8F%E7%9A%84%E6%9E%84%E5%BB%BA%E8%BF%87%E7%A8%8B "Direct link to heading")

C/C++程序生成一个可执行文件的过程可以分为4个步骤： **预处理（Preprocessing）、编译（Compiling）、汇编（Assembly）和链接（Linking）** 。

- 预处理：在编译器处理程序之前完成头文件的包含，宏扩展，条件编译，行控制等操作。
- 编译：通过词法分析和语法分析，在确认所有的指令都符合语法规则之后，将源文件代码翻译成等价的汇编代码。
- 汇编：将汇编语言代码翻译成目标机器指令，生成目标文件。
- 链接：将有关联的目标文件（以及库）相组合为一个可执行文件。

接下来，我们将通过演示实例介绍每一步发生的故事。

###### 2-0.编译工具[​](https://tars-cat.github.io/docs/gcc_g++#2-0%E7%BC%96%E8%AF%91%E5%B7%A5%E5%85%B7 "Direct link to heading")

针对不同的应用场景和平台，各大厂家设计了不同的C++编译工具。

- MSVC（Microsoft Visual C++）：MSVC是微软公司开发的C++开发工具，Visual Studio就内置了MSVC。
- GCC（GNU Compiler Collection）：GCC是由GNU（GNU's Not Unix）开发的一套编译工具，支持C、C++、Fortran、Go等一系列语言。本教程中我们使用的编译工具就是GCC。

GCC提供给用户的前端程序为 **gcc** （针对C）和 **g++** （针对C++）。它们的区别详见[gcc vs g++](https://stackoverflow.com/questions/172587/what-is-the-difference-between-g-and-gcc)。

在Linux(Ubuntu)平台上，可以使用以下指令安装上述工具：

```
sudo apt install gcc g++
```

此外还有Clang、NVCC等编译工具。不同的编译工具对C++的支持不尽然相同，此处不再赘述。

###### 2-1.预处理[​](https://tars-cat.github.io/docs/gcc_g++#2-1%E9%A2%84%E5%A4%84%E7%90%86 "Direct link to heading")

C++程序在预处理阶段会执行以下操作：宏的替换、头文件的插入、删除条件编译中不满足条件的部分。

```
g++ –E invsqrt.cpp –o invsqrt.i
```

###### 2-2.编译[​](https://tars-cat.github.io/docs/gcc_g++#2-2%E7%BC%96%E8%AF%91 "Direct link to heading")

C++程序在编译阶段会将C++文件转换为汇编文件。

```
# from .i fileg++ –S invsqrt.i –o invsqrt.s# from .cpp fileg++ –S invsqrt.cpp –o invsqrt.s
```

###### 2-3.汇编[​](https://tars-cat.github.io/docs/gcc_g++#2-3%E6%B1%87%E7%BC%96 "Direct link to heading")

汇编语言文件经过汇编，生成目标文件.o文件（二进制文件，机器码），每一个源文件都对应一个目标文件。

```
# from .s fileg++ –c invsqrt.s –o invsqrt.o# from .cpp fileg++ –c invsqrt.cpp –o invsqrt.og++ -c main.cpp -o main.o
```

> 生成的invsqrt.o 和main.o 文件不能直接打开，你可以使用 readelf -a file 阅读其信息。

###### 2-4.链接[​](https://tars-cat.github.io/docs/gcc_g++#2-4%E9%93%BE%E6%8E%A5 "Direct link to heading")

将每个源文件对应的目标.o文件链接起来，就生成一个可执行程序文件。

```
g++ invsqrt.o main.o -o main
```

当然，如果想要使用.cpp文件一步到位生成可执行文件，可以使用以下指令：

```
g++ invsqrt.cpp main.cpp -o main
```

> 在Linux系统，可执行文件一般是没有后缀名的。

###### 2-5.语法总结[​](https://tars-cat.github.io/docs/gcc_g++#2-5%E8%AF%AD%E6%B3%95%E6%80%BB%E7%BB%93 "Direct link to heading")

g++ 和gcc 工具中使用的一些命令行参数：

- -E 只进行预处理
- -S 只进行编译
- -c 只生成目标文件
- -o file 指定输出文件的名称。我们约定：.i 为预处理后的文件，.s 为汇编文件，.o 为目标文件。

###### 3.静态库和动态库[​](https://tars-cat.github.io/docs/gcc_g++#3%E9%9D%99%E6%80%81%E5%BA%93%E5%92%8C%E5%8A%A8%E6%80%81%E5%BA%93 "Direct link to heading")

出于便于复用、封装细节或防止源码泄露等原因，在实际应用过程中，我们需要把C++源码封装为库(library)。

根据其行为不同，可以将库分为静态库(static library)和动态库(shared library)。

###### 3-1.静态库[​](https://tars-cat.github.io/docs/gcc_g++#3-1%E9%9D%99%E6%80%81%E5%BA%93 "Direct link to heading")

静态库的代码在编译的过程中，会被直接载入到可执行文件中。这样做的好处是：可执行文件在执行时，不再需要静态库本身。但缺点也显而易见：生成的可执行文件的体积会比较大。

Linux平台下静态库的后缀通常为 **.a** ，命名方式通常为 **libxxx.a** ; Windows平台下静态库的后缀通常为 **.lib** 。

在Linux平台上生成静态库，并使用静态库链接形成可执行文件的方法为：

```
# generate static libar crv libinvsqrt.a invsqrt.o# link to generate the executable fileg++ -static main.cpp -L . -linvsqrt -o main_shared
```

###### 3-2.动态库[​](https://tars-cat.github.io/docs/gcc_g++#3-2%E5%8A%A8%E6%80%81%E5%BA%93 "Direct link to heading")

动态库在程序编译时并不会被连接到目标代码中，而是在程序运行是才被载入。这就带来了一个明显的好处：不同的应用程序如果调用相同的库，那么在内存里只需要有一份该共享库的实例，减小了各个模块之间的耦合程度，也减小了可执行文件的体积。然而，这也要求用户的电脑上需要同时拥有可执行文件和动态库，也有可能因为版本不匹配等问题发生DLL Hell等问题。

Linux平台下动态库的后缀通常为 **.so** ，命名方式通常为 **libxxx.so** ; Windows平台下静态库的后缀通常为 **.dll** 。

在Linux平台上生成动态库，并使用动态库链接形成可执行文件的方法为：

```
# generate shared libg++ invsqrt.cpp -I ./ -fPIC -shared -o libinvsqrt.so# move the shared library to systemsudo mv libinvsqrt.so /usr/local/lib# refreshsudo ldconfig# link to generate the executable fileg++ main.cpp -L . -linvsqrt -o main_shared.exe
```




##### Cmake
[cmake笔记](cmake笔记)
视频教学：[【从零开始详细介绍CMake】 https://www.bilibili.com/video/BV1vR4y1u77h/?p=10&share_source=copy_web&vd_source=2f6f04a1a48d1d0814f8f161d587ae67]