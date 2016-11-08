#安装ROS报告
###一、安装步骤
#####①添加 sources.list（使虚拟机能够安装来自packages.ros.org的软件包）
![image](https://cl.ly/2j2L1T2I3G1g/r1.png)

#####②添加 keys
![image](https://cl.ly/0Y3S2c3w1C2a/r2.png)

#####③安装ROS
更新Debian软件包索引

![image](https://cl.ly/1u2n0q0G0o38/r3.png)

选择桌面完整版安装

![image](https://cl.ly/2b153L0o3M25/r4.png)

初始化 rosdep(ROS核心功能组件所必需用到的工具)

![image](https://cl.ly/0C300Q350T2O/r5.png)

环境配置

![image](https://cl.ly/1c2k2f193E1h/r6.png)

安装 rosinstall

![image](https://cl.ly/3w0T0V2L0u3a/r7.png)

#####③至此，ROS算是基本安装完全

###二、实验心得

在实验过程中，遇到这样一个问题，
![image](https://cl.ly/0y0J3g0I2c06/p1.jpg)
就是虚拟机无法从官方整合包中获得个别几个包，经过上网查阅资料，发现一般这种情况可以使用wget 一个链接（http....deb)来直接获取该个包，最后重新运行该条命令检查来解决，如果不行的话，就是硬件层面的事情了。还有就是，在初始化rosdep环节，如果出现“ERROR: default sources list file already exists:”的错误，那是因为有可能之前初始化过留下记录，系统认为不必再初始化所导致的，这时候可以使用	“sudo rm -rf /etc/ros/rosdep/sources.list.d/*”来进行清除。