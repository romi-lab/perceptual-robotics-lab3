# Perceptual Robotics Lab3
In this lab, you will be learning 

* Self-localisation and mapping (SLAM)
* Potential field

## Part I: Self-localisation and mapping (SLAM)

First, run the slam package

```roslaunch xstark_nav xtarlk_slam.launch slam_methods:frontier```

Then, visulaise the result :

```rosrun rviz rviz```

Move the robot using any of the following three methods for mapping and navigation:

#### 1.Keyborad control

Connect to the driver

```roslaunch xtark_driver xtark_driver.launch```

In a new terminal, run the keyboard control node

```roslaunch xtark_ctl xtark_keyboard.launch```

The terminal(left) and control(control) are like this:

<img src="https://github.com/romi-lab/perceptual-robotics-lab3/blob/main/pictures/keyboard_terminal.png" width="400" alt=""> <img src="https://github.com/romi-lab/perceptual-robotics-lab3/blob/main/pictures/keyboard.png" width="400" alt=""> 

#### 2.Using Nav goal in Rviz

<img src="https://github.com/romi-lab/perceptual-robotics-lab3/blob/main/pictures/nav_goal.png" width="450" alt="">

#### 3.Set a region of interest using Publish Point in Rviz

<img src="https://github.com/romi-lab/perceptual-robotics-lab3/blob/main/pictures/publish_point.png" width="450" alt="">

You can then start to explore the environment. 


## Part II: Potential field

Now, close all the terimals ```ctrl + C``` and we will begin a new experiment. In this part, the car will reach the goal while avoiding the obstacles in between.
We use three AR markers to represent the car, the goal and an obstacle repectively.

<img src="https://github.com/romi-lab/perceptual-robotics-lab3/blob/main/pictures/pf_setup.png" width="450" alt="">

First, you need to launch the drvier in the car:

```roslaunch xtark_driver xtark_driver.launch```

Then run the potential field launch file:

```roslaunch xtark_ctl potentialfieldcar.launch```

In the computer, execute sendmsg.py to get the position of the car, goal and obstacle:

```python sendmsg.py```

After the car received the command, press anykey to plan potential field.
