# Ubuntu-ROS-installation2
The installation steps of Ubuntu 20.04.4 and ROS
1-Download Ubuntu 20.04.4 LTS Desktop Image from this URL: https://releases.ubuntu.com/20.04/ubuntu-20.04.4-desktop-amd64.iso

2-Download and install VirtualBox.

3-After installing VirtualBox, click New to make a new virtual machine.

4-Type Ubuntu in the field Name.

5-Set the type to Linux, and version to Ubuntu (64-bit) then click Next.

6-Set the Memory size to the end of the green bar and click Next.

7-Click Next and then click Create.

8-After creating the virtual machine we should connect Ubuntu image that we downloaded in step number 1, we do that by double clicking on the virtual machine.

9-After launching the virtual machine, click browse and choose the Ubuntu image then click Start.

10-Click Install Ubuntu then continue and wait until the installation is finished.

ROS Noetic Installation steps:
1-We should allow Ubuntu repositories (universe,multiverse,restricted). To do that, open new terminal then enter the following commands:

sudo add-apt-repository universe
then

sudo add-apt-repository multiverse
then

sudo add-apt-repository restricted
then

sudo apt-get update
2-Setup the computer to accept software from packages.ros.org by this command:

sudo apt install curl 
then

curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
then

sudo apt update
3-Install Desktop full version:

sudo apt install ros-noetic-desktop-full
4-Setup the environment by these commands:

source /opt/ros/noetic/setup.bash
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
echo "source /opt/ros/noetic/setup.zsh" >> ~/.zshrc
source ~/.zshrc
5-Install the dependencies for building packages:

sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
sudo apt install python3-rosdep
6-Initialize rosdep:

sudo rosdep init
rosdep update
Reference: http://wiki.ros.org/noetic/Installation/Ubuntu
