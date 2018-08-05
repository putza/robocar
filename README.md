# RosPiCar

This contains codebase of the earlier efforts using raspberry pi to create the autonomous capability. This runs on a framework called Robotic Operating System(ROS). The codebase contains ROS nodes that control the individual componets of the project and deep learning code for training the model.

## Rapberry Pi Setup

For Raspian compatibility pease install [raspi-config](https://larrylisky.com/2016/11/24/enabling-raspberry-pi-camera-v2-under-ubuntu-mate/):

```
$ sudo apt update
$ sudo apt upgrade
$ sudo apt install raspi-config rpi-update
```

### Graphical Remote access

Download and install [Ubuntu Mate](https://ubuntu-mate.org/download/).

Install xrdp to allow graphical access during development through RDP and VCN:

```
$ sudo apt install xrdp
```

### raspi-pi config settings:

Execute the RPi configuration using:

```
$ sudo raspi-config
```

Activate the camera, GPIOs and anything else.

Test camera (the following line needs an monitor plugged into the HDMI port):

```
$ raspivid -p 0,0,640,480 -t 0
```

# Architecture:
<img src="images/Architecture.png"/>

This version is trying to make use of [NVIDIA's End to End Deep Learning](https://devblogs.nvidia.com/deep-learning-self-driving-cars/) concept.

Please read the [medium post](https://medium.com/intro-to-artificial-intelligence/self-driving-rc-car-using-robotic-operating-system-ros-c63a6d102c08) to understand the structure of the project further.
