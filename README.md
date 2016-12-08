# Turtlebot Autonomous Exploration (3D)  and using kinect2
## modified
The code gedit from [here](https://github.com/RobustFieldAutonomyLab/turtlebot_exploration_3d),But I change it for use kinect2 and run in turtlebot. And I have change some codes, you will find it when you read the codes.It doesn't matter, you can follow origin author to download source and run the program.

## Overview

This is an ROS implementation of infomation-theoretic exploration using [turtlebot](http://wiki.ros.org/Robots/TurtleBot) with a RGBD camera (e.g. Kinect). It is designed for autonomous mapping of indoor office-like environments (flat terrain). All the computation is performed on the turtlebot laptop and intermediate results can be viewed from remote PC. The output consist of both 2D and 3D [Octomap](http://octomap.github.io/) (.ot) file and saved on the turtlebot laptop.
Link to [wiki page](http://wiki.ros.org/turtlebot_exploration_3d) (where you can find a video example.).


If you find this package useful, please consider citing the follow paper:

* S. Bai, J. Wang, K. Doherty, and B. Englot, "Inference-Enabled Information-Theoretic Exploration of Continuous Action Spaces,"Proceedings of the 17th International Symposium on Robotics Research, 16 pp., September 2015. 


## How do I get set up? 

### Download from source:

```
my_catkin_workspace/src$ git clone 
my_catkin_workspace/src$ cd ..
my_catkin_workspace$ catkin_make
```

### Configure Network:
Please follow the [turtlebot network configuration](http://wiki.ros.org/turtlebot/Tutorials/indigo/Network%20Configuration) to setup.

### Running:

From Turtlebot:
```
$ roslaunch turtlebot_exploration_3d minimal_explo.launch
$ roslaunch turtlebot_exploration_3d turtlebot_gmapping.launch
$ rosrun turtlebot_exploration_3d turtlebot_exploration_3d
```
* note: The octomap will be saved to the place where you do the "rosrun".

From Remote Server:
```
$ roslaunch turtlebot_exploration_3d exploration_rviz.launch
```

### Authors ###

Shi Bai, Xiangyu Xu.
[RFAL (Robust Field Autonomy Lab)](http://personal.stevens.edu/~benglot/index.html), Stevens Institute of Technology.

