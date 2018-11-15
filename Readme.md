# Project Racer

## Installation

```shell
cd ~/catkin_ws
catkin_make
```

## Usage

`main.launch` contains all the launch sequence without opening multiple terminals.

```shell
cd ~/catkin_ws
source devel/setup.bash
roslaunch slam_project main.launch
```

To get the RTABMSLAM mode running
```shell
roslaunch slam_project main_rtatslam.launch rtabmap_args:="--delete_db_on_start" depth_topic:=/realsense/camera/depth/image_raw rgb_topic:=/realsense/camera/color/image_raw camera_info_topic:=/realsense/camera/color/camera_info odom_topic:=/odom
```