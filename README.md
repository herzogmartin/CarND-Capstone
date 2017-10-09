Team: Millenium Vulkan
============

This is the capstone project for Udacity's Self Driving Car Nanodegree. This code is aimed to run in an actual physical self-drive vehicle.
It is the final project of the nanodegree and solved in team work.
 
### Team Members

This repository is maintained by the following:
- George Terzakis: terzakig@hotmail.com 
- Martin Herzog: martin.mh.herzog@gmail.com
- Yuda Liu: liu_yuda@163.com 
- Atul Acharya: Atul.acharya@gmail.com
- Yoni Azuelos: yonazuel@hotmail.com 

The following video shows the code in action:

[![Capstone](http://img.youtube.com/vi/1KDDv5UTwig/0.jpg)](http://www.youtube.com/watch?v=1KDDv5UTwig "CarND Capstone Project")

### Usage

1. Clone the project repository
```bash
git clone https://github.com/herzogmartin/CarND-Capstone.git
```

2. Clone the team's submodule
```bash
cd CarND-Capstone
git submodule init
git submodule update
```

3. Install python dependencies
```bash
pip install -r requirements.txt
```
4. Make and run styx
```bash
cd ros
catkin_make
source devel/setup.sh
roslaunch launch/styx.launch
```
5. Run the simulator

### Specification

The team's specification can be found [here]: https://github.com/terzakig/SelfDrivingCar3-Integration/blob/master/Vulkan_Self-Driving_Car_Capstone_Project.pdf 

### Native Installation

* Be sure that your workstation is running Ubuntu 16.04 Xenial Xerus or Ubuntu 14.04 Trusty Tahir. [Ubuntu downloads can be found here](https://www.ubuntu.com/download/desktop).
* If using a Virtual Machine to install Ubuntu, use the following configuration as minimum:
  * 2 CPU
  * 2 GB system memory
  * 25 GB of free hard drive space

  The Udacity provided virtual machine has ROS and Dataspeed DBW already installed, so you can skip the next two steps if you are using this.

* Follow these instructions to install ROS
  * [ROS Kinetic](http://wiki.ros.org/kinetic/Installation/Ubuntu) if you have Ubuntu 16.04.
  * [ROS Indigo](http://wiki.ros.org/indigo/Installation/Ubuntu) if you have Ubuntu 14.04.
* [Dataspeed DBW](https://bitbucket.org/DataspeedInc/dbw_mkz_ros)
  * Use this option to install the SDK on a workstation that already has ROS installed: [One Line SDK Install (binary)](https://bitbucket.org/DataspeedInc/dbw_mkz_ros/src/81e63fcc335d7b64139d7482017d6a97b405e250/ROS_SETUP.md?fileviewer=file-view-default)
* Download the [Udacity Simulator](https://github.com/udacity/CarND-Capstone/releases/tag/v1.2).

### Docker Installation
[Install Docker](https://docs.docker.com/engine/installation/)

Build the docker container
```bash
docker build . -t capstone
```

Run the docker file
```bash
docker run -p 127.0.0.1:4567:4567 -v $PWD:/capstone -v /tmp/log:/root/.ros/ --rm -it capstone
```

### Real world testing
1. Download [training bag](https://drive.google.com/file/d/0B2_h37bMVw3iYkdJTlRSUlJIamM/view?usp=sharing) that was recorded on the Udacity self-driving car (a bag demonstraing the correct predictions in autonomous mode can be found [here](https://drive.google.com/open?id=0B2_h37bMVw3iT0ZEdlF4N01QbHc))
2. Unzip the file
```bash
unzip traffic_light_bag_files.zip
```
3. Play the bag file
```bash
rosbag play -l traffic_light_bag_files/loop_with_traffic_light.bag
```
4. Launch your project in site mode
```bash
cd CarND-Capstone/ros
roslaunch launch/site.launch
```
5. Confirm that traffic light detection works on real life images
