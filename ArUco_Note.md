# 基于aruco进行QR码位姿的识别

ArUco：基于OpenCV的增强现实程序使用的最小库
增强现实技术（Augmented Reality，简称 AR）
The ARUCO Library has been developed by the Ava group of the Univeristy of Cordoba(Spain). It provides real-time marker based 3D pose estimation using AR markers.
aruco库由科尔多瓦大学（西班牙）的AVA组开发。它使用AR标记，提供了基于三维位姿实时估计的标记。
Uco 是Univeristy of Cordoba缩写
marker的相机pose是一个从marker坐标系统到相机坐标系统的三维变换。这是由一个旋转和一个平移向量确定的。
[ROS跟踪ArUco Markers](https://blog.csdn.net/learning_tortosie/article/details/83147232)

## １．项目地址：[aruco_ros](https://github.com/pal-robotics/aruco_ros)
```
mkdir -p ~/ArUco_ws/src
```
下载源代码并编译
```
cd ~/ArUco_ws/src
git clone https://github.com/iseedwyane/aruco_ros.git
cd .. && catkin_make
```
```
cd ~/ArUco_ws/src
svn co https://github.com/GJXS1980/Graduation_Project/trunk/aruco_ros
cd .. && catkin_make
```
## 2.修改aruco码的配置文件　
(1)在线生成aruco码　
[ArUco markers generator](http://chev.me/arucogen/)

(2)aruco的尺寸
arkerSize为aruco的尺寸大小

(3)aruco的id
markerId为aruco的id

# 
```
roslaunch aruco_ros single_realsense.launch
rqt_image_view 
rostopic echo /aruco_single/pose
```
```
rostopic hz /camera/color/image_raw
rostopic list
```

# ArUco文件夹简单解释
## bin文件夹
bin目录下有一些源码自动生成的可执行文件，像是一些demo，我们可以用它们实现ArUco的一些基本功能，比如相机标定、生成二维码、检测二维码等等。
这些可执行文件的源码都可以在你的源码包中找到，当然日后我们自己写程序的时候完全可以参考这些源码
## include文件夹
[link](https://blog.csdn.net/weixin_43053387/article/details/84952557)
## lib
是aruco的动态库。
