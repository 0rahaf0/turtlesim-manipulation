# turtlesim-manipulation
This repository provides comprehensive instructions on how to manipulate the turtlesim package in ROS Noetic.
# Turtlesim Manipulation in ROS Noetic

This repository contains instructions on how to manipulate the turtlesim package in ROS Noetic. The turtlesim package is a simple simulator for learning the basics of ROS.

## Prerequisites

- Ubuntu 20.04 or later
- ROS Noetic installed

## Getting Started

1. Start roscore

Open a terminal and run:
roscore

2.Run Turtlesim Node

In a new terminal, run:
rosrun turtlesim turtlesim_node

3. Run Turtlesim Teleop

In another terminal, run:
rosrun turtlesim turtle_teleop_key

-Use the arrow keys to move the turtle around the screen.

# Turtlesim Basic Commands

This document provides a list of basic commands for manipulating the turtlesim package in ROS Noetic, along with explanations of what each command does.

1.Running the Turtlesim Node

run this command:
rosrun turtlesim turtlesim_node

2.Controlling the Turtle with Keyboard

run this command:
rosrun turtlesim turtle_teleop_key

3.Spawning a New Turtle
You can spawn additional turtles in the simulator using the service call:

run this command:
rosservice call /spawn 5 5 0 "turtle2"

-Description: Spawns a new turtle at coordinates (5, 5) with an initial orientation of 0 radians and names it "turtle2".

4.Moving the Turtle to a Specific Position

To move the turtle to a specific position, use the following command:
rostopic pub /turtle1/cmd_vel geometry_msgs/Twist -r 1 -- '[2.0, 0.0, 0.0]' '[0.0, 0.0, 1.8]'

-Description: Publishes a velocity command to the turtle, moving it forward with a linear speed of 2.0 and rotating it with an angular speed of 1.8.


5.Drawing a Circle

To make the turtle draw a circle, use the following command:
rostopic pub /turtle1/cmd_vel geometry_msgs/Twist -r 1 -- '[2.0, 0.0, 0.0]' '[0.0, 0.0, 2.0]'

-Description: Publishes a velocity command to the turtle, causing it to move in a circular path.

6.Changing the Background Color

To change the background color of the simulator, use the following parameter setting:
rosparam set /turtlesim/background_b 255
rosservice call /clear

-Description: Sets the blue component of the background color to 255 (maximum), turning the background blue. Then, clears the screen to apply the new background color.

<img width="617" alt="ros2-done" src="https://github.com/user-attachments/assets/27f982f7-c39f-467a-b148-083ae6809c5d">
