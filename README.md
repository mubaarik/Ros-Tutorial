

1. Installing and configuring your invironment </br>

2. Installing Ros-kenetic </br>
	* Configure your Ubuntu repositories to allow "restricted," "universe," and "multiverse." </br>
	* Set up the keys </br>
		`sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116` </br>
	* Install </br>
		  `sudo apt-get update` </br>
		  `sudo apt-get install ros-kinetic-desktop-full` </br>
	* Initialize rosdep </br>
		  `sudo rosdep init` </br>
		  `rosdep update`  </br>
	* Environment setup </br>
		  `echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc` </br>
		  `source ~/.bashrc` </br>
3. Ros workspaces([catkin workspace](http://wiki.ros.org/catkin/workspaces)), packages, and files 
	* ROS workspaces
	ROS uses [catkin](http://docs.ros.org/api/catkin/html/) to build packages, but to tell catkin what packages to build you need to create a workspace, essentially a directory that contains all the packages to be build. a catkin workspace is a special directory that is recognizable by ROS via the ROS tree. Which means you need to run special commands to make it.
		* Creating cakin workspace
	
4. The ROS communication system( Nodes, Topics, and messages).
5. ROS commands 
6. Creating workspaces, packages, and Nodes.
7. Racecar sensor anatomy 
8. Running Gazebo 
9. Running the racecar 
10. ROS GUIs
11. Bag-files 
12. Common errors and possible solutions 
13. 
