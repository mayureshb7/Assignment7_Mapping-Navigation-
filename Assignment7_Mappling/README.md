This file describes mapping and navigation of a Turtlebot3 Burger on Gazebo and Real world


*Part 1 - Mapping & Navigation - Real World*

	1) Gmapping and Navigation
		a) Run Roscore on the pc terminal
		b) Bring up turtlebot3 burger by using this command on turtlebot terminal: roslaunch turtlebot3_bringup turtlebot3_robot.launch
		c) Run command: "rosrun map_server map_saver -f ~/gmap" in different terminal for execution of gmapping in real world environment (Map available in Assignment7_Mapping/maps)
		d) Define the pose in RVIZ for navigation
	
	2) Karto Map & Navigation
		a) Run Roscore on the pc terminal
		b) Bring up turtlebot3 burger by using this command on turtlebot terminal: roslaunch turtlebot3_bringup turtlebot3_robot.launch
		c) Run command: "rosrun map_server map_saver -f ~/kartomap" in different terminal for execution of gmapping in real world environment (Map available in Assignment7_Mapping/maps)
		d) Define the pose in RVIZ for navigation	
		
*Part 2 - Mapping & Navigation using two different LIDAR (LDS & 2D Hukoyo)- Gazebo World*

	1) Mapping and Navigation using LDS Lidar
		Mapping:
		1) Run command: "roslaunch Assignment7_Mappling slam_gmap.launch"
		2) Navigate the turtlebot to create a map
		3) Save the map using this command in another terminal: "rosrun map_server map_saver -f ~/gmap_lds"
		
		Navigation:
		a) Run command: "roslaunch turtlebot3_gazebo turtlebot3_world.launch" to launch the world"
		b) In another terminal run command "roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/gmap.yaml"
		c) Define the pose in RVIZ for navigation
		
	2) Mapping and Navigation using Hukoyo 2D Lidar
	
		Mapping:
		1) Run command: "roslaunch Assignment7_Mappling slam_gmap.launch"
		2) Navigate the turtlebot to create a map
		3) Save the map using this command in another terminal: "rrosrun map_server map_saver -f ~/hukoyo_map"
		
		Navigation:
		1) Mapping and Navigation using Hukoyo Lidar
		a) Run command: "roslaunch turtlebot3_gazebo turtlebot3_world.launch" to launch the world"
		b) In another terminal run command "roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/hukoyo_map.yaml"
		c) Define the pose in RVIZ for navigation
		
	Difference in between two LIDAR for mapping and navigation:
		1) Gmapping by LDS lidar shows better capability in tracing out the obstacles accurately than the 2D Hukoyo LIDAR
		2) LDS Lidar mapping gave clear edge detection of the map than the Hukoyo LIDAR
	
	Refer to videos for demonstration of above tasks from Assignment7_Mappling/videos
	Refer to view and use maps from Assignment7_Mappling/maps
