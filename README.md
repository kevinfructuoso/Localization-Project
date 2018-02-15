# Where Am I? Localization Project

In this project, the goal is to implement the Adaptive Monte Carlo Localization (AMCL) method in order to determine a robots pose within the Robot Operating System (ROS). A custom ROS package was built leveraging the AMCL and Move Base ROS packages to localize a custom-defined robot in order to complete this project.

# Project Setup
For this setup, catkin_ws is the name of the active ROS workspace. If your workspace name is different, change the commands accordingly.

If you do not have an active ROS workspace, you can create one by:

```sh
$ mkdir -p ~/catkin_ws/src
$ cd ~/catkin_ws/
$ catkin_make
```

Now that you have a workspace, clone or download this repo into the src directory of your workspace:
```sh
$ cd ~/catkin_ws/src
$ git clone https://github.com/udacity/RoboND-Perception-Project.git

Now install missing dependencies using rosdep install:
```sh
$ cd ~/catkin_ws
$ rosdep install --from-paths src --ignore-src --rosdistro=kinetic -y
```
Build the project:
```sh
$ cd ~/catkin_ws
$ catkin_make
```

If you haven’t already, following line can be added to your .bashrc to auto-source all new terminals
```sh
source ~/catkin_ws/devel/setup.bash
```

To run the package, open two terminals and ensure both have been sourced as in the above step. To launch the Gazebo and RViz nodes, enter the following in the first terminal window:
```sh
$ cd ~/catkin_ws
$ roslaunch udacity_bot udacity_world.launch
```

To start the localization, enter the following in the second terminal window:
```sh
$ cd ~/catkin_ws
$ roslaunch udacity_bot amcl.launch
```

In order to run a navigation test, open another terminal window:
```
$ cd ~/catkin_ws
$ rosrun udacity_bot navigation_goal
``` 
