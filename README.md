# Install-of-ROS-Noetic

# Overview of ROS (Robot Operating System)

ROS (Robot Operating System) is an open-source framework that simplifies robotic software development. It provides tools and libraries for seamless communication between software components. While not a traditional operating system, it acts as middleware for complex robot applications.

## Key Features

- **Open-Source**: Freely available for modification and distribution.
- **Middleware**: Facilitates communication between various software components.
- **Optimized for Ubuntu**: Leverages Ubuntu's package management and community support.
  
# Installing ROS on Ubuntu 20.04

This README outlines the steps I took to install ROS (Robot Operating System) on Ubuntu 20.04, serving as a guideline to help you with your installationhow to change

### Step 1: Open the Terminal
I opened the terminal in my Ubuntu virtual machine to run the commands below to install ROS
![Image](https://github.com/user-attachments/assets/58ad5344-e9cb-4f06-b6eb-278a83061e3c)

## Step 2: Set Up Your Sources List
In the terminal, I run the following command:
```bash
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```

## Step 3: Set Up Your Keys
1- First, First, I ensure I have curl installed. but if you haven't installed it yet,  run
```
sudo apt install curl
```
2-Then, add the ROS key using the following command:
```
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```
## Step 4: Update Package Index
I run the following command to update my package index
```
sudo apt update
```
## Step 5: Install ROS
Desktop-Full Install 
```
source /opt/ros/noetic/setup.bash
```
## Step 6: Environment Setup
I set up my environment by running:
```
source /opt/ros/noetic/setup.bash
```
```
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```
## Step 7: Install Dependencies for Building Packages
```
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```

## Step 8: Initialize rosdep
Before using many ROS tools,  I initialize rosdep by running
```
sudo rosdep init
rosdep update
```
### By the end of these commands, I have successfully installed ROS Noetic on Ubuntu 20.04.
