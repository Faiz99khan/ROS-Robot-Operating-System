# ROS-Robot-Operating-System
**What is ROS**

According to *wiki.ros.org*

ROS is an **open-source, meta-operating system for your robot.** It provides the services you would expect from an operating system, including hardware abstraction, low-level device control, implementation of commonly-used functionality, message-passing between processes, and package management. It also provides tools and libraries for obtaining, building, writing, and running code across multiple computers. ROS is similar in some respects to 'robot frameworks,' such as Player, YARP, Orocos, CARMEN, Orca, MOOS, and Microsoft Robotics Studio.

It is defined in other words at https://www.ros.org/about-ros/

ROS is a flexible framework for writing robot software. It is a collection of tools, libraries, and conventions that aim to simplify the task of creating complex and robust robot behavior across a wide variety of robotic platforms.

<img src="images/ros.png" width="500"> <br/>
[Image credit](https://towardsdatascience.com/what-why-and-how-of-ros-b2f5ea8be0f3)
<br/>
<br/>

**Why**

Because creating truly robust, general-purpose robot software is hard. From the robot's perspective, problems that seem trivial to humans often vary wildly between instances of tasks and environments. Dealing with these variations is so hard that no single individual, laboratory, or institution can hope to do it on their own.
<br/>
<br/>

**Goals**

 The primary goal of ROS is to support code *reuse* in robotics research and development
 
 In support of this primary goal of sharing and collaboration, there are several other goals of the ROS framework:

*Thin*:  ROS is designed to be as thin as possible -- we won't wrap your main() -- so that code written for ROS can be used with other robot software frameworks. A corollary to this is that ROS is easy to integrate with other robot software frameworks: ROS has already been integrated with OpenRAVE, Orocos, and Player. <br/>
*ROS-agnostic libraries*:  the preferred development model is to write ROS-agnostic libraries with clean functional interfaces.<br/>
*Language independence*:  the ROS framework is easy to implement in any modern programming language. We have already implemented it in Python, C++, and Lisp, and we have experimental libraries in Java and Lua. <br/>
*Easy testing*:  ROS has a builtin unit/integration test framework called rostest that makes it easy to bring up and tear down test fixtures.
*Scaling*:  ROS is appropriate for large runtime systems and for large development processes.

for more information click [here](http://wiki.ros.org/ROS/Introduction) 


# Installation on Ubuntu
**Step-1 Choose a ROS distribution**

The following ROS distributions are pretty common, but there are many others apart from these.
If you want to run two or more at a same time, you can do that as well.

[<img target="_blank" src="images/d1.PNG" >](http://wiki.ros.org/kinetic/Installation) [<img target="_blank" src="images/d2.PNG" >](http://wiki.ros.org/melodic/Installation) [<img target="_blank" src="images/d3.PNG" >](http://wiki.ros.org/noetic/Installation)
<br/>
<br/>

**Step-2 Select the platform as a Ubuntu**

If you choose *Noetic ROS distribution*, you will see the result like this. 
<img target="_blank" src="images/platform.PNG" >
<br/>
<br/>

**Step-3.1 Configure your Ubuntu repositories**

Configure your Ubuntu repositories to allow "restricted," "universe," and "multiverse." You can follow [the Ubuntu guide for instructions](https://help.ubuntu.com/community/Repositories/Ubuntu) on doing this.
<br/>
<br/>

**Step-3.2 Setup your sources.list**

Setup your computer to accept software from packages.ros.org.
```bash
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```
<br/>
<br/>

**Step-3.3 Set up your keys**
```bash
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
```
If you experience issues connecting to the keyserver, you can try substituting hkp://pgp.mit.edu:80
<br/>
<br/>

**Step-3.4 Keep Debian package index up-to-date**
```bash
sudo apt update
```
<br/>
<br/>

**Step-3.5 Actual installation**
     
Desktop-Full Install: (Recommended) : Everything in Desktop plus 2D/3D simulators and 2D/3D perception packages
```bash
sudo apt install ros-noetic-desktop-full
```

OR

Desktop Install: Everything in ROS-Base plus tools like rqt and rviz.
```bash
sudo apt install ros-noetic-desktop
```
<br/>
<br/>

**Step-3.6 Environment setup**

You must source this script in every bash terminal you use ROS in.
```bash
source /opt/ros/noetic/setup.bash
```
You can set to automatically source this script every time a new shell is launched by following command.
```bash
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```
<br/>
<br/>

**Step-3.7 Dependencies for building packages**

Up to now you have installed what you need to run the core ROS packages. To create and manage your own ROS workspaces, there are various tools and requirements that are distributed separately. For example, rosinstall is a frequently used command-line tool that enables you to easily download many source trees for ROS packages with one command.

To install this tool and other dependencies for building ROS packages, run:
```bash
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```
**Step-3.7.1 Initialize rosdep**

Before you can use many ROS tools, you will need to initialize rosdep. rosdep enables you to easily install system dependencies for source you want to compile and is required to run some core components in ROS. If you have not yet installed rosdep, do so as follows
```bash
sudo apt install python3-rosdep
```
With the following, you can initialize rosdep.
```bash
sudo rosdep init
rosdep update
```











