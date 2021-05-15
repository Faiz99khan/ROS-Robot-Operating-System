# ROS-Robot-Operating-System

# Installation
**Step-1 Choose a ROS distribution**

The following ROS distributions are pretty common, but there are many others apart from these.
If you want to run two or more at a same time, you can do that as well.

[<img target="_blank" src="images/d1.PNG" >](http://wiki.ros.org/kinetic/Installation) [<img target="_blank" src="images/d2.PNG" >](http://wiki.ros.org/melodic/Installation) [<img target="_blank" src="images/d3.PNG" >](http://wiki.ros.org/noetic/Installation)

**Step-2 Select the platform as a Ubuntu**

[<img target="_blank" src="images/platform.PNG" >]()


**Step-3.1 Configure your Ubuntu repositoriesu**

Configure your Ubuntu repositories to allow "restricted," "universe," and "multiverse." You can follow [the Ubuntu guide for instructions](https://help.ubuntu.com/community/Repositories/Ubuntu) on doing this.


**Step-3.2 Setup your sources.list**

Setup your computer to accept software from packages.ros.org.
```bash
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```


**Step-3.3 Set up your keys**
```bash
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
```
If you experience issues connecting to the keyserver, you can try substituting hkp://pgp.mit.edu:80


**Step-3.4 Keep Debian package index up-to-date**
```bash
sudo apt update
```
**Step3.5 Actual installation**
     
Desktop-Full Install: (Recommended) : Everything in Desktop plus 2D/3D simulators and 2D/3D perception packages
```bash
sudo apt install ros-noetic-desktop-full
```

OR

Desktop Install: Everything in ROS-Base plus tools like rqt and rviz.
```bash
sudo apt install ros-noetic-desktop
```








