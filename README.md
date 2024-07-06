# Installing Ubunto
1- We need first to install VirtualBox the last version 7.0.18: [VirtualBox Download](https://www.virtualbox.org/)<br>

2- Since Ubunto 20.04 us compatible with all features and functions we need to work on such as ROS1 and ROS2, we will downlaod this version: [Ubunto Download](https://releases.ubuntu.com/focal/) <br>

Double check on the link you download from.<br>
<img src="https://github.com/Layan002/AI-Task1-Installing-Ubunto-and-ROS/assets/107956591/8e734244-6fe5-499c-85b0-07246d30c4fb" alt="Image description" width="400"><br>

3- Open VirtualBox and insert the unziped file of the Ubunto Operating System (OS) to the virtual machine.<br>

Desktop interface:<br>
<img src="https://github.com/Layan002/AI-Task1-Installing-Ubunto-and-ROS/assets/107956591/eca58da6-80d3-4fbe-a7a7-dab178ae8f84" alt="Image description" width="400"><br>
 

# Installing ROS1
1- To install ROS1, Open your Ubunto OS in the Virtual Machine, then follow the description in [this page](https://wiki.ros.org/noetic/Installation/Ubuntu) carefully. DONT just copy paste the commands on the terminal shell. In addition, I strongly recommend you to use ChatGPT if you encountered any problem.<br> 

2- Extra explination from me for some commands:<br>
- Before installing any peckage of Debian-based Linux distributions (such as Ubuntu). These commands are so important since they manage software packages and keep your system up-to-date and avoid many errors and problems you may encounter, use the following commands:
```bash
sudo apt update
sudo apt upgrade
```
- It is recommended to install the Desktop-Full as I did. Because When you install the "Desktop-Full" package of ROS (Robot Operating System), you get a comprehensive set of tools and libraries that include everything in the standard desktop installation plus additional simulators and perception packages.
```bash
sudo apt install ros-noetic-desktop-full
```
<p align="center">
  <img src="https://github.com/Layan002/AI-Task1-Installing-Ubunto-and-ROS/assets/107956591/38503ef5-96c9-433e-b580-d01dcc136b79" alt="First Image" width="45%" style="margin-right: 10px;">
  <img src="https://github.com/Layan002/AI-Task1-Installing-Ubunto-and-ROS/assets/107956591/08518757-4c6a-47b2-bd13-2ec3fb91e0d2" alt="Second Image" width="45%">
</p>

# Checking the successful instullation of ROS1 

After completting ROS installation, operate some commands on the Ubunto terminal to check everything were installed successfully:<br>
- Make sure your ROS environment variables are set. You can do this by sourcing your ROS setup file:<br>
```bash
source /opt/ros/noetic/setup.bash
```
- To make this change permanent, you can add the above line to your ~/.bashrc file:
```bash
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```
- Check ROS Environment Variables:<br>
```bash
printenv | grep ROS
```
You should see something like this: <br>
<img src="https://github.com/Layan002/AI-Task1-Installing-Ubunto-and-ROS/assets/107956591/8e0b768b-7da6-4afd-bd07-5f83e1ac894a" alt="image" width="400"> <br>
- Check ROS Version - Run the following command to check the installed ROS version: <br>
``` bash
rosversion -d
```
This should output 'noetic'. <br>
- Start the ROS master node to ensure that ROS is functioning correctly: <br>
``` bash
roscore
```
Output: <br>
<img src="https://github.com/Layan002/AI-Task1-Installing-Ubunto-and-ROS/assets/107956591/586aa40c-6f4c-4e81-9025-631aada60448" alt="image" width="400"> <br>
- Install some commonly used ROS packages:
``` bash
sudo apt install ros-noetic-common-msgs ros-noetic-ros-base ros-noetic-ros-comm
```
- Create a Catkin Workspace - testing Create a new directory for your workspace and initialize it:
``` bash
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/
catkin_make
```
Output: <br>
<img src="https://github.com/Layan002/AI-Task1-Installing-Ubunto-and-ROS/assets/107956591/6fae7a24-46b7-4a01-85d3-021e8abed806" alt="image" width="400"> <br>
- Source the setup file for your workspace: <br>
``` bash
source devel/setup.bash
```
- To make this change permanent, you can add the above line to your ~/.bashrc file: <br>
``` bash
echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
source ~/.bashrc
```
- Create a simple ROS package to test your installation: <br>
``` bash
cd ~/catkin_ws/src
catkin_create_pkg test_pkg std_msgs rospy roscpp
cd ~/catkin_ws
catkin_make
```
- In a new terminal, start roscore if it's not already running:
``` bash
roscore
```
- Open another terminal and run a simple ROS node: <br>
``` bash
cd ~/catkin_ws
source devel/setup.bash
roscd test_pkg
roscpp_tutorials talker
```
<img src="https://github.com/Layan002/AI-Task1-Installing-Ubunto-and-ROS/assets/107956591/ef081311-f99f-49f1-ab84-bc060fdab9da" alt="image" width="400"> <br>

If you've done all of these commands and get their outputs, you can start with ROS. Congratulations !


















