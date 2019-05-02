# Usage of double_cam_stream

## Requirements
- Ubuntu 18.04 LTS (could be VM, work on MacOS host with Parallels Desktop,
    not works on macOS with VMWare 11 (camera has lags), not tested with VirtualBox)
- ROS Melodic, Desktop-Full Install (Installation guide http://wiki.ros.org/Installation/Ubuntu)
- Created catkin workspace http://wiki.ros.org/ROS/Tutorials/InstallingandConfiguringROSEnvironment

## Installation

- Run `echo "source /home/youuser/catkin_ws/devel/setup.bash" >> ~/.bashrc`
- Restart terminal
- Check enviroment variables
        `$ echo $ROS_PACKAGE_PATH
         /home/youruser/catkin_ws/src:/opt/ros/melodic/share`
- `cd ~/catkin_ws/src`
- Install dependency 'usb_cam' `sudo apt-get install ros-melodic-usb-cam`
- Clone forked `image_pipeline` repo: `git clone https://github.com/givip/image_pipeline`
- Clone repo: `git clone https://github.com/givip/double_cam_stream.git`
- `cd ~/catkin_ws`
- `catkin_make`

## Run locally publisher node
- `cd ~/catkin_ws/src/double_cam_stream/launch/usb_cam/`
- `roslaunch double_cam_publisher.launch`

## Run locally subscriber node
- `cd ~/catkin_ws/src/double_cam_stream/launch/usb_cam/`
- `roslaunch double_cam_subscriber.launch`
