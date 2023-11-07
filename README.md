# Micro_mouse

## Overview

This project aims to find the shortest path of a maze using the picture of the maze obtained using an overhead camera. The shortest path is found using Breadth For Search (BFS) Algorithm.
Once the shortest path is calculated, the (x,y) coordinates are used to move the differential drive bot using a JointVelocityController.  The position of the robot is obtained as the feedback from
Gazebo states. All the elements of the program were integrated with ROS as the middleware.

## System Specifications

OS version: Ubuntu 18.04 LTS

ROS Version: ROS Melodic

## Folder Breakdown

### Config

- Contains the information on the JointStateController and the JointVelocityController.

### launch 

- gazebo.launch file consists of all the elements to run the project using a single launch file. It spawns the maze, the differential drive robot, and the node that controls the drive.

### scripts

- differential_drive.py is the python script that contains the node micro_mouse_controller that is responsible for the control of the differential drive bot in the gazwebo environment.
- shortest_path.npy is a numpy file that contains all the points that correspond to the shortest path of the maze.

### urdf

- Contains the description file of the robot.

### world

- Contains the description of the maze file.
