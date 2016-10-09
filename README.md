#**第一次报告**   
<br/>
###一、DOL 框架描述
####通过实验分布式操作层（DOL）是一个框架，基本上由三部分组成：
####1.应用程序编程
DOL定义了一组计算和通信程序，使对形状分布平台，并行应用程序的编程。使用这些程序，应用程序员可以编写程序，而无需了解底层架构的详细知识。事实上，这些程序都受限于硬件相关的软件（HDS）层进一步完善。
####2.仿真功能
提供程序员可能性测试其应用程序，功能仿真框架已经形成。除了应用功能验证，这个框架是用来在应用程序级获得的性能参数。
####3.映射优化
DOL映射优化的目标是计算一组在一种SHAPES结构平台上的应用的最佳映射。在第一步骤中，基于XML规范格式已定义允许以描述一个抽象级别的应用程序和体系结构。尽管如此，所有必要获取的信息，都应该包含准确的性能估计信息。
<br/>
<br/>
###二、DOL安装心得
1.实验环境

主机系统为window10 64位专业版，所用虚拟机软件为VMware Workstation 12 Player，所用ubuntu版本如下图所示

![image](https://cl.ly/0r091q1b111Y/1.png)

2.配置环境下载解压文件步骤省略

3.编译systemc

进入systemc-2.3.1的目录下

    cd systemc-2.3.1

新建一个文件夹objdir

    mkdir objdir

进入文件夹objdir

    cd objdir

运行configure

    ../configure CXX=g++ --disable-async-updates

运行之后如下图

![image](https://cl.ly/1Z3u1r3n0u1U/2.png)

编译

    sudo make install

编译完后查看文件夹目录

    ls

如下图

![image](https://cl.ly/3S411l2z070u/3.png)

记录当前的工作路径

    pwd

路径如下图

![image](https://cl.ly/1c3l1b2Y0Y2D/4.png)

4.编译dol

进入dol文件夹

    cd ../dol

修改build_zip.xml文件，如下图（由于系统为64位，所以将lib-linux改成lib-linux64）

![image](https://cl.ly/3A1l2h1A3P2K/5.png)
<br/>
![image](https://cl.ly/0F0L3I2z3m0P/6.png)

编译

    ant -f build_zip.xml all

编译成功，结果如下图

![image](https://cl.ly/2R0x3N3d1e1R/7.png)

试运行第一个例子

进入build/bin/mian路径下

    cd build/bin/main
	ant -f runexample.xml -Dnumber=1

运行成功，结果如下图

![image](https://cl.ly/0p1z1K1c1I3s/8.png)
<br/>
<br/>
###三、实验心得
在本次实验中，遇到了这么一个问题，在进行“运行configure”的步骤时，终端报了这样一个错误“C++ compiler cannot create executables...”，在网上搜索了相关博客之后，试了许多种方法，最后发现了一个正确的方法

![image](https://cl.ly/3y2z040T3i2M/9.png)

通过这次实验，我对DOL框架有了实践层面上的一个认识，而不是局限于书本层面上的，并且对linux的指令有了更深入的理解。

