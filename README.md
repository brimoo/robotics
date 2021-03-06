# Robotics

Code for CSE180: Intro to Robotics

## Requirements

ROS is required to run this project. Installing ROS(kinetic or newer) on an Ubuntu system is recommended,
but it is possible to install on other operating systems.

## Building

Run `catkin_init_workspace` inside of the src directory and two folders will be created in the base 
workspace directory, build and devel. In order for ROS to know where your workspace is, you will either 
need to run `source devel/setup.bash` once per terminal, or put this command inside of your bashrc. 
For zsh users, the command is `source devel/setup.zsh`.

## Running

Due to the large degree of variance between each lab/project some are run differently than others. Below
are instructions to run each individual project/lab.

**Lab 1:** Simply use the launch file by enetring `roslaunch labpkg lab1.launch` from anywhere.

**Lab 2:** First enter `roslaunch husky_gazebo husky_empty_world.launch` to launch the simulator and then enter `rosrun labpkg square` and enjoy watching a robot move in a square(almost).
       
**Lab 3:** First enter`roslaunch husky_gazebo husky_playpen.launch` to launch the simulator, then enter `rosrun labpkbg getpose` and then enter `rosrun labpkg gotopose`. The terminal you entered the second command in will prompt you to enter a pose for the robot to move to. Do this and watch the robot attempt to move to the pose you select in the simulator.

**Lab 4:** First enter `roslaunch husky_gazebo multi_husky_playpen.launch` to launch the simulator, then enter `rosrun random random` and then enter `rosrun labpkg repeat` and watch a robot attempt to mimic the moves of another robot. Additionally, you can enter `rosrun labpkg listener` to see a live print out of the transforms being received by the husky_alpha bot.

**Lab 5:** This lab is just an improved version of lab 3. First enter `roslaunch husky_gazebo huskylab5.launch` to launch the simulator, then enter `rosrun labpkg getpose`. You can now choose to run gotopose or gotoposetimeout by entering `rosrun labpkg gotopose` or `rosrun labpkg gotoposetimeout`.

**Lab 6:** First enter `roslaunch husky_gazebo huskylab5.launch` to launch the simulator. Then enter `rosrun labpkg saferandomwalk` and watch the robot move around the environment randomly and stop whener it detects that it is within 0.2 meters of an obstacle. You can also run `rosrun labpkg detectdivergence` in parallel with the previous node, this will stop the robot if the sensor readings diverge too much.

**Lab 7:** First enter `roslaunch husky_gazebo huskyfinal.launch` to launch the simulated environment. Then enter `rosrun labpkg saferandomwalk` to get the robot moving around randomly. Then enter `rosrun labpkg uncertainty`, and watch as the terminal spits out the volume of the uncertainty ellipsoid that represents the covariance matrix of the localization estimator.
