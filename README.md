# MEAM_5200_Pick_and_Place_Final_Project

## Overview

Developed as the final project for MEAM 5200 Introduction to Robotics, a graduate robotics course at the University of Pennsylvania. The goal of this project was to develop an autonomous robotic system capable of identifying, grasping, and stacking both static and moving blocks using a Franka Panda robotic arm. The system integrated computer vision, kinematics, motion planning, and manipulation, and vas validated on physical hardware while under a time-based competition scoring system.

> Source code is not included due to course policies.

## My Contributions

- Developed the static block pick-and-stack pipeline 
- Optimized dynamic acquisition by tuning perception, grasp timing, and robot motion
- Imrpoved execution speed by reducing unnecessary inverse kinematic calculation and adding fixed poses
- Tested and calibrated hardware to account for camera offsets and simulation-to-real differences
- Evaluated system performance and iterated based on hardware testing

## Technologies

- ROS
- Python
- Franka Panda Robot
- AprilTags + Computer Vision
- Forward and Inverse Kinematics
- Motion Planning


## What I Learned

### Balancing between Efficiency and Redundancy
Because the challenge was time-constrained, we balanced computational efficiency with robustness. Rather than recomputing every pose, we leveraged precomputed poses and known constraints where appropriate to maximize throughput while maintaining reliable manipulation.

### Hardware calibration

Simulation did not perfectly match the physical robot. We calibrated camera offsets and modified observation poses to improve localization accuracy, and wrote the code to allow for easy day-of calibration from different robots. 

### Dynamic manipulation
Capturing moving blocks required balancing arm speed with timing accuracy while accounting for the rotating platform.

## Results

The final system successfully

- stacked 4/4 static blocks
- successfully grasped and stacked dynamic blocks from the rotating platform
- demonstrated repeatable autonomous pick-and-place behavior on the Franka Panda arm

![Demo](videos/static.gif)

...
