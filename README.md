# 10704912_autonomous_nav
Simulation of a robot that is capable of autonomous navigation of a unknown map while avoiding obstacles.
# System requirements
* Ubuntu16_04
* CoppeliaSim_V4_1_0_Ubuntu16_04

# How to run the system
* Create a new folder called Programs in home folder.
* Download the version required of CoppeliaSim software if you don't have it from the coppeliaSim website.
* Copy CoppeliaSim to the Programs folder.
* Open a new termianl and type the following command:\
  - gedit .bashrc (This command will open a file named .bashrc which is a shell script. This script is used to initialize an interactive shell session. It contains commands to set up the shell for use in your particular environment or to customize the session.)
  - Go to the end of the file and add the following lines of codeexport COPPELIASIM_ROOT_DIR=~/Programs/CoppeliaSim_Edu_V4_1_0_Ubuntu16_04alias coppeliaSim="cd $COPPELIASIM_ROOT_DIR && ./coppeliaSim.sh" 
  - Save the file and exit.
* Download autonomous_navigation_wss from this repositories.
* autonomous_navigation_wss.tar shoild appera in your Downloads folder.
* Copy this file in your home folder and extract it.
* Copy libv_repExtRos.so which can be found in the lib subfolder of the devel folder of the turtlebot_simulation workspace in autonomous_navigation_wss to the main folder of CoppeliaSim.
* Open a new terminal and start ROS by typing roscore.
* Open a new terminal and type coppeliaSim to start coppeliaSim software.
* Check in the terminal where you opened coppeliaSim if the ROS libraries have been successfully loaded (you should see: plugin 'ROSInterface':load succeeded)
* In coppeliaSim open the turtlebot_maze_scenario.ttt which can be found in autonomous_navigation_wss/turtlebot_simulation/src/vrep_simulation/scenes
* Play the simulation
* Open a new terminal, ensure that you are in autonomous_navigation_wss and type the following command:
  - source source_all.bash
  - roslaunch turtlebot_gmapping turtlebot_gmapping.launch
* Open a new terminal, ensure that you are in autonomous_navigation_wss and type the following command:
  - source source_all.bash
  - roslaunch turtlebot_rviz_launchers turtlebot_rviz.launch
* Open a new terminal, ensure that you are in autonomous_navigation_wss and type the following command:
  - source source_all.bash
  - roslaunch turtlebot_navigation move_base.launch
* Open the rviz software and click on "2D Nav Goal" button and click on the goal that you want the robot to navigate to.

# Improvments
* Adding another robot to the environment and implementing a no-collision system between the two robots to allow autonomous navigation in a dynamic environment could be considered. 
* Integration of a more complicated map and a robot with more sensors for greater spatial understanding of the map might be another addition.
