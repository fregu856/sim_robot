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
Add "source ~/sim_robot/catkin_ws/devel/setup.bash" to the bottom of ~/.bashrc ($ sudo nano ~/bashrc) for this line to be run everytime you open the terminal (otherwise you have to do it manually).  

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

Simulation in Gazebo:  
$ cd sim_robot/catkin_ws/src  
$ git clone https://github.com/StanfordASL/asl_turtlebot.git  
Add "export GAZEBO_MODEL_PATH=~/sim_robot/catkin_ws/src/asl_turtlebot/models" to the bottom of ~/.bashrc ($ sudo nano ~/bashrc) for this line to be run everytime you open the terminal (otherwise you have to do it manually).  

Test the simulation:  
$ roslaunch asl_turtlebot turtlebot_sim.launch  
If this doesn't work, open another terminal and do this FIRST:  
$ rosrun gazebo_ros gzclient  

Run a test controller to check that everything is working:  
Place "test_controller.py" in sim_robot/catkin_ws/src/turtlebot_control/scripts, make it executable and build the package.  
$ roslaunch asl_turtlebot turtlebot_sim.launch  
$ rosrun turtlebot_control test_controller.py (in another terminal)  
The robot should now move to the coordinate (1, 1).    




