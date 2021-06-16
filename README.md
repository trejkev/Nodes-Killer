# Nodes-Killer
ROS node intended to take a snap of the map and save it into ~/Documents/Maps/ when the FlaggerNode dies, and finally kill all the nodes that are running.

Notes:
1. Default FlaggerNode is /speed_controller, which comes from this repo: https://github.com/LauraRincon/nav_node
2. The node gives some time before starting to dig into ROS active nodes, looking for the FlaggerNode presence. It can be modified through warmupTime variable, which is defaulted to 5 seconds, but it can be insufficient if the computer has limited resources.
3. The user has to make sure that the directory ~/Documents/Maps/ exists, there the map will be saved as 'SLAM_Map_{Date and time}'.
4. The node was developed for ROS Melodic.
