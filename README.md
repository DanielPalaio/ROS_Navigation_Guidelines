# ROS Navigation Guidelines

Tutorial to rapidly start exploring **ROS**, **Gazebo** and **RViz** by controlling a robot, using the keyboard, in simulated environments.  

Some ROS basics are described in this repository as well.  

## Ubuntu 

To install Ubuntu (desktop version), consult the following repository:  
https://github.com/DanielPalaio/Ubuntu_Setup  

## ROS

To install ROS, consult the following ROS.org page:  
http://wiki.ros.org/noetic/Installation/Ubuntu  

## RViz

To install RViz, open the Ubuntu Terminal and follow the commands below:  
> sudo apt update  
> sudo apt install rviz  

## Turtlebot3 Package  

To install the turtlebot3 package, consult the following tutorial:   
https://automaticaddison.com/how-to-launch-the-turtlebot3-simulation-with-ros/  

## Catkin Workspace  

To built ROS packages, a **catkin workspace** in required. To create a workspace,  
> source /opt/ros/noetic/setup.bash  
> mkdir -p ~/catkin_ws/src  
> cd ~/catkin_ws/  
> catkin_make  
> source devel/setup.bash  
> echo $ROS_PACKAGE_PATH  

## Catkin Package

> cd ~/catkin_ws/src  
> catkin_create_pkg pkg_name std_msgs rospy roscpp  
> cd ~/catkin_ws  
> catkin_make  
> . ~/catkin_ws/devel/setup.bash  

## Python File  

> cd ~/catkin_ws/src/pkg_name/src  
> gedit python.py  
> chmod +x python.py  
> rosrun pkg_name python.py  

## ROS MSG File  

> cd ~/catkin_ws/src/pkg_name  
> mkdir msg  
> cd msg  
> gedit message.msg  
> cd ~/catkin_ws/src/pkg_name  
> In package.xml:  
>> Uncomment <build_depend>message_generation</build_depend> and  <exec_depend>message_runtime</exec_depend>  

> In CMakeLists.txt:  
>> Add message_generation to find_package()  
>> Uncomment add_message_files() and add message.msg  
>> Uncomment generate_messages()  
>> Add message_runtime to catkin_package() CATKIN DEPENDS  

> cd ~/catkin_ws
> catkin_make
> . ~/catkin_ws/devel/setup.bash
> In python.py:	
>> from pkg_name.msg import message

## Turtlebot3 + Gazebo + Rviz + teleop control

> source /opt/ros/noetic/setup.bash  
> roscore		

> source /opt/ros/noetic/setup.bash  
> cd ~/catkin_ws/src  
> source ~/catkin_ws/devel/setup.bash  
> cd turtlebot3_simulations/turtlebot3_gazebo/launch  
> roslaunch turtlebot3_world.launch  

> source /opt/ros/noetic/setup.bash  
> cd ~/catkin_ws/src  
> source ~/catkin_ws/devel/setup.bash  
> cd turtlebot3/turtlebot3_teleop/launch  
> roslaunch turtlebot3_teleop_key.launch  

> source /opt/ros/noetic/setup.bash  
> cd ~/catkin_ws/src  
> source ~/catkin_ws/devel/setup.bash  
> cd turtlebot3_simulations/turtlebot3_gazebo/launch  
> roslaunch turtlebot3_gazebo_rviz.launch  



