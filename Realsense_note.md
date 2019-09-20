# Realsense D415的驱动
## 步骤一：安装Realsense SDK2.0 
[官网教程](https://github.com/IntelRealSense/librealsense/blob/master/doc/distribution_linux.md#installing-the-packages) 
查询realsense pkg version
```
$ dpkg -l | grep realsense
```

## 步骤二：安装Realsense ROS功能包
1.创建工作空间
```
mkdir -p ~/sensor_ws/src
cd ~/sensor_ws/src/
```
２．下载realsense-ros源码包
```
git clone https://github.com/IntelRealSense/realsense-ros.git
git clone https://github.com/pal-robotics/ddynamic_reconfigure.git
```
3编译源码包
```
cd ~/sensor_ws && catkin_make
echo "source ~/sensor_ws/devel/setup.bash" >> ~/.bashrc
source ~/.bashrc
```
4.测试 (1)启动rgb相机
```
roslaunch realsense2_camera rs_camera.launch
```
## [Debug:issue](https://github.com/IntelRealSense/librealsense/issues?utf8=%E2%9C%93&q=Frame+metadata+isn%27t+available%EF%BC%81)

```
sudo apt-get update
sudo apt-get upgrate
```
```

git clone https://github.com/IntelRealSense/realsense-ros.git
cd ~/sensor_ws && catkin_make
```
