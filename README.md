# Autonomous Car with ROS2 Humble

This project implements an autonomous car using ROS2 Humble. The repository contains two packages: `camera_viewer` and `localization`.

## Overview

### Packages

- **camera_viewer**: Contains a script to open the camera on a Raspberry Pi connected to a Jetson and transmit the video feed on a ROS topic.
- **localization**: Contains the necessary files to run localization using a launch file (`puzzlebot_rviz.launch.py`). Additionally, the `localization` script within this package must be run at the end.

### Functionality

The code in this repository enables the robot to:
1. Find a cube.
2. Approach and pick up the cube.
3. Deliver the cube to point A, B, or C based on the detected Aruco marker.

The robot uses a Kalman filter with lidar and Aruco markers to correct its pose.

### Requirements

- ROS2 Humble
- A differential drive robot with encoder velocity feedback
- A lidar sensor
- A package to process the lidar point cloud
- A package for detecting Aruco markers

## Setup

1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/andrea2702/Autonomous_car_ROS2_Humble.git
   
2. Run the puzzlebot_rviz.launch.py launch file from the localization package:
  ```bash
  ros2 launch localization puzzlebot_rviz.launch.py
  ```
3. Run the localization script within the localization package.


## Demo
A video demonstration of the project is available below:
[![Demo del Proyecto](http://img.youtube.com/vi/YZyWaMJPywo/0.jpg)](https://www.youtube.com/watch?feature=shared&v=YZyWaMJPywo)

