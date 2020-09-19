# Basic 2R Manipulator URDF + Gazebo Simulation

## This is the basic 2R manipulator robot package for ROS URDF testing and Gazebo simulation testing 

The package is ment to be used as a fast way to test a simple simulation in Gazebo and also provide a base reference for creating URDF models form sratch using Xacro (XML Macros). 

![2R RVIZ](https://i.ibb.co/vxqcyXh/2R-RVIZ.png)

## Prerequisites

Tested on **Ubuntu 20.04** with **ROS Noetic** full desktop installation. ( [ROS Installation](http://wiki.ros.org/noetic/Installation/Ubuntu))

_**Dependencies for URDF RViz visualization:**_

* [_urdf_](http://wiki.ros.org/urdf)
* [_joint_state_controller_](http://wiki.ros.org/joint_state_controller)
* [_robot_state_publisher_](http://wiki.ros.org/robot_state_publisher)

This packages are already included in the full desktop installation, alongside [RViz](http://wiki.ros.org/rviz) the 3D visualization tool for ROS.

_**Aditional dependencies for Gazebo simulation:**_

* [_controller_manager_](http://wiki.ros.org/ros_control)

The _controller_manager_ is part of the _ros_control_ set, to install the set use:

```bash
sudo apt-get install ros-noetic-ros-control ros-noetic-ros-controllers
```
In addition the simulation will run on [Gazebo](http://gazebosim.org/) (simulation tool for robotics), it is included in the full desktop ROS installation, but it can be downloaded [here](http://gazebosim.org/download).



## Installation
To install this package clone the repository in your ROS workspace (usually `~/catkin_ws/`). Build the workspace and source the new files.

## Usage
To use the URDF model for RViz visualization, use:

```bash
roslaunch basic_2r_gazebo rviz.launch 
```
To simulate the model in Gazebo, first start a `roscore`, then in new shell initialize Gazebo:

```bash
rosrun gazebo_ros gazebo  
```
Finally in anothe shell, launch the model in the simulator:

```bash
roslaunch basic_2r_gazebo spawn.launch 
```


## Authors 

* **Jurgen Krejci** - [JurgenHK](https://github.com/JurgenHK) - Initial Work 

## Contributing
Feel free to fork and clone this repo, this is the list of issues, fixes and other features that need a to be worked or reviewed: 

- [ ] Review and modify `spawn.launch`, Gazebo and ROS should be initilized from the launch file
- [ ] Test on ROS Melodic (Collect Issues and provide support)
- [ ] Test on ROS Kinetic (Collect Issues and provide support)




