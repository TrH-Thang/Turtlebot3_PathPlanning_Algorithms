# Path Planning Repository for custom robot

## Overview
This repository utilizes path planning algorithms for navigation. This README provides instructions on how to set up and run the simulation. Follow this website for more details: https://emanual.robotis.com/docs/en/platform/turtlebot3/navigation/https://emanual.robotis.com/docs/en/platform/turtlebot3/navigation/

## Setup

### 1. Clone Repository
Clone the Turtlebot3 and path planning repositories using the following commands:

```bash
https://github.com/ROBOTIS-GIT/turtlebot3.git
```
```bash
https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
```
```bash
https://github.com/TrH-Thang/Turtlebot3_PathPlanning_Algorithms.git
```
after cloning do catkin_make

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
roslaunch path_planning path_planning.launch
```
It will open a rviz window select 2D Nav Goal button and select the goal position on the map.

In the path_planning/scripts/path_planning_server.py file, locate line 42 and change the algorithm to your desired one (e.g., astar, dijkstra, rrt).
