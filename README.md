# Install-package-in-ROS

we we want run a robotic arm by cloning an existing project from GitHub, from here (Smart Methods)[https://github.com/smart-methods]


-
### Setup your computer to accept software from packages.ros.org
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```
### Set up your keys
```
sudo apt install curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```
### First, make sure your Debian package index is up-to-date
```
sudo apt-get update
```
### Desktop-Full Install: (Recommended) : Everything in Desktop plus 2D/3D simulators and 2D/3D perception packages
```
sudo apt-get install ros-noetic-desktop-full
```
### Environment setup
```
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc

source ~/.bashrc
```
```
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```
```
sudo apt install python3-rosdep
```
```
sudo rosdep init
```
```
rosdep update
```
```
mkdir -p ~/catkin_ws/src
```
```
cd ~/catkin_ws/
```
```
catkin_make
```
```
cd ~/catkin_ws/src
```

### clone the project from github
```
git clone https://github.com/smart-methods/arduino_robot_arm.git 
```
```
cd ~/catkin_ws
```
```
rosdep install --from-paths src --ignore-src -r -y
```
```
sudo apt-get install ros-noetic-moveit
```
```
sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
```
```
sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
```
```
sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
```
```
catkin_make
```
### Launching ROS on a project from @Smart_methods for a robotic arm
```
roslaunch robot_arm_pkg check_motors.launch
```
## then done!!!
<img width="540" alt="176787831-7a983435-8aca-4f8d-afcd-36c967d1b654" src="https://user-images.githubusercontent.com/109445693/179381996-0435898f-8167-4191-8d5b-7cb9567fb583.png">
