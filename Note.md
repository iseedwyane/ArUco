# 基于aruco进行QR码位姿的识别

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
