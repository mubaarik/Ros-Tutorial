

1. Installing and configuring your invironment </br>

1. Installing Ros-kenetic </br>
	a. Configure your Ubuntu repositories to allow "restricted," "universe," and "multiverse." </br>
	b. Set up the keys </br>
		`sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116` </br>
	c. Install </br>
		  `sudo apt-get update` </br>
		  `sudo apt-get install ros-kinetic-desktop-full` </br>
	d. Initialize rosdep </br>
		  `sudo rosdep init` </br>
		  `rosdep update`  </br>
	e) Environment setup </br>
		  `echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc` </br>
		  `source ~/.bashrc` </br>
