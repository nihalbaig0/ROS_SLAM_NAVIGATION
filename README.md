# ROS SLAMNAVIGATION
-----

## Install ROS NAVIGATION and SLAM in ROS NOETIC

Open a terminal and type :

`sudo apt-get install ros-noetic-navigation`

`sudo apt-get install ros-noetic-slam-gmapping`

## Installing TurtleBOT3 

`sudo apt-get update`

`sudo apt-get upgrade`

$ cd ~/catkin_ws/src/

$ git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git -b noetic-devel

$ git clone  https://github.com/ROBOTIS-GIT/turtlebot3.git -b noetic-devel

$ cd ~/catkin_ws && catkin_make

After compilation of catkin_ws

/catkin_ws/src/

$ git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git

$ cd ~/catkin_ws && catkin_make

Then modify .bashrc file

cd

gedit .bashrc

Inside the bashrc file put the following aliases to make it easier access to different executables in the alias section.

alias burger='export TURTLEBOT3_MODEL=burger'

alias waffle='export TURTLEBOT3_MODEL=waffle'

alias tb3fake='roslaunch turtlebot3_fake turtlebot3_fake.launch'

alias tb3teleop='roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch'

alias tb3='roslaunch turtlebot3_gazebo turtlebot3_empty_world.launch'

alias tb3maze='roslaunch turtlebot3_gazebo turtlebot3_world.launch'

alias tb3house='roslaunch turtlebot3_gazebo turtlebot3_house.launch'

also at the end of the file, write the following commands

source /opt/ros/noetic/setup.bash

source /home/akoubaa/catkin_ws/devel/setup.bash

export TURTLEBOT3_MODEL=waffle

export SVGA_VGPU10=0

## Starting TurtleBot3 

`roslaunch turtlebot3_gazebo turtlebot3_house.launch`

`roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=/home/nihal/catkin_ws/src/ros_course_part2/src/topic03_map_navigation/tb3map/tb3_house_map.yaml`

## View frames error

Simply adding the .decode('utf-8') to m = r.search(vstr.decode('utf-8')) fixed it.

`roslaunch turtlebot3_gazebo turtlebot3_gazebo_rviz.launch`
