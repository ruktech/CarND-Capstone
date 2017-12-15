![Banner](images/udacity_banner.png)
![Logo](images/team_banner.PNG)

This repository contains the results of Team "Wow That Was Fast"'s capstone project for the [Udacity Self-Driving Car Engineer Nanodegree Program](https://www.udacity.com/drive). The project utilizes Ubuntu Linux 14.04 with [Robot Operating System (ROS)](https://www.ros.org) Indigo and/or Ubuntu Linux 16.04 with ROS Kinetic, the [Udacity System Integration Simulator](https://github.com/udacity/CarND-Capstone/releases), and code written in C++ and Python to provide a System Integration solution to the self-driving car problem. The code developed will be tested on Udacity's real-world test vehicle (a Lincoln MKZ that the company has named "Carla") during December 2017. 

#### Check out our results in the Udacity simulator:

[[![YouTube](https://img.youtube.com/vi/4lzDBvFPQMM/0.jpg)](https://www.youtube.com)]


### Team Members
|     Name    |      Location     |     LinkedIn     |          |
|-------------|-------------------|------------------|----------|
| Kyle Martin <br> (**Team Lead**) | Phoenix, Arizona | [linkedin.com/in/kylemart](https://www.linkedin.com/in/kylemart) | <img src="./images/kyle.png" alt="Kyle" width="150" height="150"> |
| Farrukh Ali | Los Angeles, California | [linkedin.com/in/farrukhtech](https://www.linkedin.com/in/farrukhtech) | <img src="./images/farrukh.png" alt="Farrukh" width="150" height="150"> |
| Michael Matthews | Sydney, Australia | [linkedin.com/in/michael-matthews-59378933](https://www.linkedin.com/in/michael-matthews-59378933) | <img src="./images/michael.png" alt="Michael" width="150" height="150"> |
| Daniel Kröhnert | Duesseldorf, Germany | [linkedin.com/in/daniel-kröhnert-411235128](https://www.linkedin.com/in/daniel-kr%C3%B6hnert-411235128) | <img src="./images/daniel.png" alt="Daniel" width="150" height="150"> |
| Jordan Lee | Tucson, Arizona | [linkedin.com/in/TBD](https://www.linkedin.com/in/TBD/) | <img src="./images/jordan.png" alt="Jordan" width="150" height="150"> |



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
docker run -p 4567:4567 -v $PWD:/capstone -v /tmp/log:/root/.ros/ --rm -it capstone
```

### Usage

1. Clone the project repository
```bash
git clone https://github.com/kylemartin1/CarND-Capstone.git
```

2. Install python dependencies
```bash
cd CarND-Capstone
pip install -r requirements.txt
```
3. Make and run styx
```bash
cd ros
catkin_make
source devel/setup.sh
roslaunch launch/styx.launch
```
4. Run the simulator

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
