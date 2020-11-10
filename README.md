# Basic 2R Manipulator URDF + Gazebo Simulation

## This is the basic 2R manipulator robot package for ROS URDF testing and Gazebo simulation testing 

The package is ment to be used as a fast way to test a simple simulation in Gazebo and also provide a base reference for creating URDF models form scratch using Xacro (XML Macros). 

![2R Robot](https://i.ibb.co/vxqcyXh/2R-RVIZ.png)

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
To install this package clone the repository in your ROS workspace (usually `~/catkin_ws/src/`). Build the workspace and source the new files.

## Usage
To use the URDF model for RViz visualization, use:

```bash
roslaunch basic_2r_gazebo rviz.launch 
```
![2R_Rviz](https://i.ibb.co/fGsWMRX/2-R-Rviz-Window.png)

To simulate the model in Gazebo, use:

```bash
roslaunch basic_2r_gazebo 2r_gazebo.launch
```
![2R_Gazebo](https://i.ibb.co/9GtXdRs/Screenshot-from-2020-10-16-00-56-32.png)

For double robots in Gazebo, use:

```bash
roslaunch basic_2r_gazebo double_2r_gazebo.launch
```
![2R_Gazebo_Double](https://i.ibb.co/HxyhLsZ/2r-gazebo-double.png)

## Authors 

* **Jurgen Krejci** - [JurgenHK](https://github.com/JurgenHK) - Initial Work 

## Contributing
Feel free to fork and clone this repo. This is the list of issues, fixes and other features that need a to be worked or reviewed: 

- [x] Review and modify `2r_gazebo.launch`, Gazebo and ROS should be initilized from the launch file
- [x] Test on ROS Melodic (Collect Issues and provide support)
- [x] Test on ROS Kinetic (Collect Issues and provide support)




