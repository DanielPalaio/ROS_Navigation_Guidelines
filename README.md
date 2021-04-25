# ROS Navigation Guidelines

Tutorial to rapidly start exploring **ROS**, **Gazebo** and **RViz**.  

## Ubuntu 

To install Ubuntu (desktop version), consult the following repository:  
https://github.com/DanielPalaio/Ubuntu_Setup  

## ROS

To install ROS, consult the ROS.org page below:  
http://wiki.ros.org/noetic/Installation/Ubuntu  

## RViz

To install RViz, open the Ubuntu Terminal and follow the commands below:  
> sudo apt update  
> sudo apt install rviz  

## Turtlebot3 Package  

To install the turtlebot3 package, consult the following tutorial:   
https://automaticaddison.com/how-to-launch-the-turtlebot3-simulation-with-ros/  

## Turtlebot3 + Gazebo + Rviz + teleop control

> **Open new Terminal**   
>> source /opt/ros/noetic/setup.bash  
>> roscore		

> **Open new Terminal**   
>> source /opt/ros/noetic/setup.bash  
>> cd ~/catkin_ws/src  
>> source ~/catkin_ws/devel/setup.bash  
>> cd turtlebot3_simulations/turtlebot3_gazebo/launch  
>> roslaunch turtlebot3_world.launch  

> **Open new Terminal**   
>> source /opt/ros/noetic/setup.bash  
>> cd ~/catkin_ws/src  
>> source ~/catkin_ws/devel/setup.bash  
>> cd turtlebot3/turtlebot3_teleop/launch  
>> roslaunch turtlebot3_teleop_key.launch  

> **Open new Terminal**   
>> source /opt/ros/noetic/setup.bash  
>> cd ~/catkin_ws/src  
>> source ~/catkin_ws/devel/setup.bash  
>> cd turtlebot3_simulations/turtlebot3_gazebo/launch  
>> roslaunch turtlebot3_gazebo_rviz.launch  



