

1. Installing and configuring your invironment 

1. Installing Ros-kenetic
	a) Configure your Ubuntu repositories to allow "restricted," "universe," and "multiverse." 
	b) Set up the keys 
		`sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116`
	c) Install
		`sudo apt-get update`
		`sudo apt-get install ros-kinetic-desktop-full`
	d) Initialize rosdep
		`sudo rosdep init`
		`rosdep update`
	e) Environment setup
		`echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc`
		`source ~/.bashrc`
