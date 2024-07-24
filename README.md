# Path Planning Repository for custom Turtlebot3

## Overview
This repository utilizes path planning algorithms for navigation. This README provides instructions on how to set up and run the simulation. 
Follow this website for more details: https://wiki.ros.org/ROS/Tutorials

## Setup

### 1. Clone Repository
Clone the Turtlebot3 and path planning repositories using the following commands:

```bash
cd ~/catkin_ws/src
https://github.com/ROBOTIS-GIT/turtlebot3.git
https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
https://github.com/TrH-Thang/Turtlebot3_PathPlanning_Algorithms.git
catkin_make
```

### 2. Launch Simulation
Please use the proper keyword among burger, waffle, waffle_pi for the TURTLEBOT3_MODEL parameter.

ex:

open a terminal and run following command
```bash
export TURTLEBOT3_MODEL=waffle
```
then:

```bash
roslaunch turtlebot3_gazebo turtlebot3_world.launch
```
### 3. Launch Navigation with different Path Planning algorithms
To enable navigation with different path planning algorithms, run the following command:
```bash
export TURTLEBOT3_MODEL=waffle
roslaunch path_planning path_planning.launch
```
It will open a rviz window select 2D Nav Goal button and select the goal position on the map.

In the path_planning/scripts/path_planning_server.py file, locate line 42 and change the algorithm to your desired one (e.g., astar, dijkstra, rrt).

