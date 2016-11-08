#体验一cartographer报告
###一、安装步骤
①安装依赖项

![image](https://cl.ly/3t1s3U3Z0f1y/C1.png)

②创建工作区并初始化

![image](https://cl.ly/1E071h1z071f/C2.png)

③下载cartographer_ros

![image](https://cl.ly/0A2v3a1M2g38/C3.png)

④安装依赖项

![image](https://cl.ly/2U1g3q0J2U2X/C4.0.png)

结果为

![image](https://cl.ly/0q1Z2T3L0739/C4.5.png)

⑤开始安装

![image](https://cl.ly/0Y0N2Y0E1y1A/C5.png)

⑥下载2D和3D demo

依次输入如下指令下载demo

	wget -P ~/Downloads https://storage.googleapis.com/cartographer-public-data/bags/backpack_2d/cartographer_paper_deutsches_museum.bag

	wget -P ~/Downloads https://storage.googleapis.com/cartographer-public-data/bags/backpack_3d/cartographer_3d_deutsches_museum.bag

⑦至此，cartographer基本安装成功

###二、实验结果截图

运行2D demo

	roslaunch cartographer_ros demo_backpack_2d.launch bag_filename:=${HOME}/Downloads/cartographer_paper_deutsches_museum.bag

![image](https://cl.ly/3F3o0D3a0x2o/2D.png)

运行3D demo

	roslaunch cartographer_ros demo_backpack_3d.launch bag_filename:=${HOME}/Downloads/cartographer_3d_deutsches_museum.bag

![image](https://cl.ly/3I1V041R2J2V/3D1.jpg)

红线部分

![image](https://cl.ly/2c3s2314253o/3D2.jpg)

怀疑是网络问题，导致无法显示3D图。

###实验感想
通过这次实验，对ubuntu指令更加熟悉，并且初步了解了cartographer的作用以及应用领域，更加熟悉ROS。