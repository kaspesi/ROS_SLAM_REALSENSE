## CSE 360 Final Project Submission Repo 

Implementation of Simultanous Locilization and Mapping in ROS for Autonomous Vehical Project


### Build Requirements
* ROS Melodic
* Ubuntu 18.04 (Jeston Image)
* Catkin
* Eigen3

### Hardware Requirements 
* IntelRealsense Depth camera
* Jetson Xavier NX board 

#### Setting up ROS Melodic and ROS Dependincies 
```
$ sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
$ sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
$ sudo apt update
$ sudo apt install ros-melodic-desktop-full
$ apt search ros-melodic
$ echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
$ source ~/.bashrc
$ sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential
$ sudo rosdep init
$ rosdep update
```

### Setting up Catkin 
```
$ sudo apt-get install ros-lunar-catkin
$ sudo apt-get install python-catkin-tools
```
### Other dependencies
```
sudo apt install libeigen3-dev
```
### Building Project
```
$ cd /.../Repo_Directory
$ catkin_make
$ . ~/catkin_ws/devel/setup.bash
$ catkin build 
```
### Running SLAM
For visualization RVIZ can be used
```
sh startCamera.sh
sh startSlam.sh
```
### Published Topics

#### SLAM ROS node
* /orb_slam2_ros/PointCloud2
* /orb_slam2_ros/PoseStamped
* /orb_slam2_ros/image
* /orb_slam2_tf (For transformations)

##### Camera ROS node (RealSense)
* /camera/color/camera_info
* /camera/color/image_raw
* /camera/depth/camera_info
* /camera/depth/image_rect_raw
* /camera/extrinsics/depth_to_color
* /camera/extrinsics/depth_to_infra1
* /camera/extrinsics/depth_to_infra2
* /camera/infra1/camera_info
* /camera/infra1/image_rect_raw
* /camera/infra2/camera_info
* /camera/infra2/image_rect_raw
* /camera/gyro/imu_info
* /camera/gyro/sample
* /camera/accel/imu_info
* /camera/accel/sample
* /diagnostics

### Subscribed Topics
* /camera/image_raw
* /camera/depth_registered/image_raw
* /camera/rgb/camera_info
* /image_left/image_color_rect
* /image_right/image_color_rect
* /image_left_camera_info


### License
```
@article{murORB2,
  title={{ORB-SLAM2}: an Open-Source {SLAM} System for Monocular, Stereo and {RGB-D} Cameras},
  author={Mur-Artal, Ra\'ul and Tard\'os, Juan D.},
  journal={IEEE Transactions on Robotics},
  volume={33},
  number={5},
  pages={1255--1262},
  doi = {10.1109/TRO.2017.2705103},
  year={2017}
 }
 ```
