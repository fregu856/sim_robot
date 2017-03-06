# sim_robot

Needed:  

Ubuntu 16.04.1  
ROS Kinetic  
ros-kinetic-turtlebot  
ros-kinetic-turtlebot-apps  
ros-kinetic-turtlebot-interactions  
ros-kinetic-turtlebot-simulator  
catkin

Catkin:  
Create a workspace:  
http://wiki.ros.org/catkin/Tutorials/create_a_workspace  

Create a package in the workspace:  
$ cd sim_robot/catkin_ws/src
$ catkin create pkg turtlebot_control std_msgs roscpp rospy
$ cd sim_robot/catkin_ws
$ catkin make  

Every script that you write must be made executable:  
$ chmod a+x script.py  
You should also build the package:  
$ cd sim_robot/catkin_ws  
$ catkin_make

