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

<img src="https://github.com/Layan002/AI-Task1-Installing-Ubunto-and-ROS/assets/107956591/38503ef5-96c9-433e-b580-d01dcc136b79" alt="image" width="400"> <br>
<img src="https://github.com/Layan002/AI-Task1-Installing-Ubunto-and-ROS/assets/107956591/08518757-4c6a-47b2-bd13-2ec3fb91e0d2" alt="image" width="400"> <br>



3- After completting ROS installation, operate some commands on the Ubunto terminal to check everything were installed successfully:<br>
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
<img src="https://github.com/Layan002/AI-Task1-Installing-Ubunto-and-ROS/assets/107956591/8e0b768b-7da6-4afd-bd07-5f83e1ac894a" alt="image" width="400"> <br>










