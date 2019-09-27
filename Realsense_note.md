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
#bug
```
roslaunch aruco_ros single_realsense.launch
```
```
Failed to load nodelet [/camera/realsense2_camera] of type [realsense2_camera/RealSenseNodeFactory] even after refreshing the cache: Failed to load library /home/lisen/sensor_ws/devel/lib//librealsense2_camera.so. Make sure that you are calling the PLUGINLIB_EXPORT_CLASS macro in the library code, and that names are consistent between this macro and your XML. Error string: Could not load library (Poco exception = librealsense2.so.2.28: cannot open shared object file: No such file or directory)
[ERROR] [1569584523.184041881]: The error before refreshing the cache was: Failed to load library /home/lisen/sensor_ws/devel/lib//librealsense2_camera.so. Make sure that you are calling the PLUGINLIB_EXPORT_CLASS macro in the library code, and that names are consistent between this macro and your XML. Error string: Could not load library (Poco exception = librealsense2.so.2.28: cannot open shared object file: No such file or directory)
[FATAL] [1569584523.184216556]: Failed to load nodelet '/camera/realsense2_camera` of type `realsense2_camera/RealSenseNodeFactory` to manager `realsense2_camera_manager'
[camera/realsense2_camera-3] process has died [pid 2939, exit code 255, cmd /opt/ros/kinetic/lib/nodelet/nodelet load realsense2_camera/RealSenseNodeFactory realsense2_camera_manager __name:=realsense2_camera __log:=/home/lisen/.ros/log/c9beec2a-e11b-11e9-8f38-00d8617d3e94/camera-realsense2_camera-3.log].
log file: /home/lisen/.ros/log/c9beec2a-e11b-11e9-8f38-00d8617d3e94/camera-realsense2_camera-3*.log
```


