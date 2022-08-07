# task1- task2
First I downloaded The virtual boxes version 6.1 , then created a new file named " ros_an". Downloaded the ubuntu version 20.04.4 and followed the instruction. Opened the terminator and past the steps in this link to install ROS into the ubuntu
http://wiki.ros.org/noetic/Installation/Ubuntu
1-Setup Ubuntu repositories sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
2-Setup the keys If you haven't already installed curl
Desktop-Full Install: (Recommended) : Everything in Desktop plus 2D/3D simulators and 2D/3D perception packages sudo apt install ros-noetic-desktop-full Desktop Install: Everything in ROS-Base plus tools like rqt and rviz sudo apt install ros-noetic-desktop ROS-Base: (Bare Bones) ROS packaging, build, and communication libraries. No GUI tools. sudo apt install ros-noetic-ros-base If we want to install a specific package we can use this command:
sudo apt install ros-noetic-PACKAGE NAME Also, to find the other available packages, use:
apt search ros-noetic 4. Setup the enviroment we should source this scipt in every bash terminal we use ROS in. but in my opinion, practically it's not convenient.
source /opt/ros/noetic/setup.bash It will be more convenient to automatically source this script every time er launched a new shell. There are couple of commands that will do that for us.
Bash echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc source ~/.bashrc Zsh echo "source /opt/ros/noetic/setup.zsh" >> ~/.zshrc source ~/.zshrc 5. Dependencies for building packages To install the tool and other dependencies for building ROS packages, run:
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential 5.1. Initialize rosdep If you have not yet installed rosdep, use:
sudo apt install python3-rosdep Initialize rosdep and update it
sudo rosdep init rosdep update
