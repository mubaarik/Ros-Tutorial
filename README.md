

1. Installing and configuring your invironment </br>

2. Installing Ros-kenetic </br>
	* Configure your Ubuntu repositories to allow "restricted," "universe," and "multiverse." </br>
	* Set up the keys </br>
		```js
		sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116``` </br>
	* Install </br>
		  `sudo apt-get update`</br>
		  `sudo apt-get install ros-kinetic-desktop-full` </br>
	* Initialize rosdep </br>
		  `sudo rosdep init` </br>
		  `rosdep update`  </br>
	* Environment setup </br>
		  `echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc` </br>
		  `source ~/.bashrc` </br>
3. Ros workspaces([catkin workspace](http://wiki.ros.org/catkin/workspaces)), packages, and files 
	* ROS workspaces(catkin workspace)
	ROS uses [catkin](http://docs.ros.org/api/catkin/html/) to build packages, but to tell catkin what packages to build you need to create a workspace, essentially a directory that contains all the packages to be build. a catkin workspace is a special directory that is recognizable by ROS via the ROS tree. Which means you need to run special commands to make it. 
		* Creating cakin workspace </br>
		```mkdir -p ~/name_of_your_workspace/src```</br>
		```cd ~/name_of_your_workpace/``` </br>
		```catkin_make``` </br>
	* ROS packages(catkin package)
	If workspace(catkin workspace in this case) was just the directory to store your packages, package essentially stores files for a particular project(e.g. lab), but again it is a ros package for a reason. Along with your files it contains two special files [package.xml](http://wiki.ros.org/catkin/package.xml), and [CMakelists.txt](http://wiki.ros.org/catkin/CMakeLists.txt). 
		* Creating catkin package</br>
		`cd ~/name_of_your_workspace/src`</br>
		`catkin_create_pkg name_of_your_package [depend1] [depend2] [depend3]`</br>
		
		
	
4. The ROS communication system( Nodes, Topics, and messages).
	* ROS Node is essentially a process that performs a computation(e.g. a Python script that computes the distance between two points). If you're familiar with Python or other functional/object oriented programming languages, you know that different parts of your program communicate via function or method calls. Essentially one function or a method does some computation and produces some output, and then other function that needs that output calls. The problem with is the fact that if one of those functions or methods in a sequence of calls contains a problem and crushes, it usually leads to everything crushing. This is a big problem for something like a self-driving car or drone. It means that if not usiful script crushes at some point in a mission, you just lost you robot or endangered lives. ROS is the way to avoid that disaster. ROS Nodes which are essentially classes or functions of some programming language communicating via topics. You can think of topic as frequency on the radio band and nodes as radioes broadcasting on those frequencies. Nodes publishes messages on chosen topics and other nodes can (subscribe) or listen to that topic and use message data to do their calculations and then publishes messages of their own on some topic. If one node crushes it doesn't effect others, except the onces that was listening to what it was publishing may not be able to do their computation.  
5. ROS commands 
	* Listing nodes, topics and messages.</br>
		* rosnode commands </br>
			`$ rosnode info /node_name`  #Displays out information about the node, like subscriptions and publications</br>
			`$ rosnodes list`	#Displays the names of all the running nodes.</br>
			`$ rosnode list /my_namespace`	#Displays out all the nodes in this namespace</br>
		* rostopic commands.</br>
			`rostopic list` #Display all used topics</br>
			`rostopic echo /topic_name` #Displays messsages published on the topic</br>
			`rostopic hz /topic_name` #Display the publishing rate of a topic.</br>
		* rosmsg commands</br>
			`rosmsg list` #Display a list of all messages</br>
			`rosmsg show <message_name>` #Display the fields in a ROS message type.</br>
			
6. Creating workspaces, packages, and Nodes.
	* With that short introduction to ros, let's start with creating a workspace for this tutorial. We will call our workpace rss_tutorial_ws</br?>
	`mkdir -p ~/rss_tutorial_ws/src`</br>
	`cd ~/rss_tutorial_ws`</br>
	`catkin_make`</br>
	* If everything went according to plan, you should two more directories(build, devel) created in the workspace. Now let's create a package, we called it tutorial_lab0. This package has the depends rospy, std_msgs, geometry_msgs,  sensor_msgs </br>
	`cd ~/rss_turorial_ws/src`</br>
	`catkin_create_pkg tutorial_lab0 rospy std_msgs geometry_msgs  sensor_msgs`</br>
	
	* If you navigate into rss_turorial_ws/src, you should see that the a directory with appropriate name is created. As we mensioned earlier, every package has two required files(`CMakeLists.txt  package.xml`), make sure that they are present.</br> 
7. Racecar sensor anatomy 
8. Running Gazebo 
9. Running the racecar 
10. ROS GUIs
11. Bag-files 
12. Common errors and possible solutions 
13. 
