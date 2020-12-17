## CSE 360 Final Project Submission Repo 

Implementation of Simultanous Locilization and Mapping in ROS for Autonomous Vehical Project


### Build Requirements
* ROS Melodic
* Ubuntu 18.04

#### Setting up ROS Melodic and ROS Dependincies 
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
sudo apt update
sudo apt install ros-melodic-desktop-full
apt search ros-melodic
echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
source ~/.bashrc
sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential
sudo rosdep init
rosdep update
```

#### Setting up Catkin 
```
sudo apt-get install ros-lunar-catkin
sudo apt-get install python-catkin-tools
```
