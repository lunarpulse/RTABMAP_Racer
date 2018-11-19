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

roslaunch slam_project main_rtatslam.launch rtabmap_args:="--delete_db_on_start" rviz:=true
roslaunch slam_project teleop.launch
rtabmap-databaseViewer ~/.ros/rtabmap.db

```

Debug time

```shell

source devel/setup.bash

roslaunch slam_project world.launch
roslaunch slam_project teleop.launch
roslaunch slam_project rtabslam.launch rtabmap_args:="--delete_db_on_start" rtabmapviz:=false rviz:=true amcl:=true
roslaunch slam_project rtabviz.launch
rtabmap-databaseViewer ~/.ros/rtabmap.db

```