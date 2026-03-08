# Week 1 ROS2 Lab

## Introduction
In this lab, I learned the basics of ROS 2 including how to create a workspace, build packages, and run a simple node. The goal was to understand the ROS 2 development environment and how nodes can be executed.

## Commands Used
mkdir -p ~/ros2_ws/src  
cd ~/ros2_ws  
colcon build  
source install/setup.bash  
ros2 pkg create --build-type ament_python my_first_pkg  
ros2 pkg list | grep my_first_pkg  
ros2 run my_first_pkg simple_node  

## What I Learned
Through this lab I understood how ROS 2 organizes projects using workspaces and packages. I also learned how to create a Python node and run it using ROS 2 commands.

## Reflection
This lab helped me understand the basic workflow of ROS 2 development. Setting up the workspace and building packages showed how ROS 2 manages projects. Running the simple node demonstrated how nodes execute inside the ROS environment.
