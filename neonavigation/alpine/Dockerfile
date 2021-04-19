FROM ghcr.io/alpine-ros/alpine-ros:noetic-bare

RUN apk add --no-cache \
  ros-${ROS_DISTRO}-neonavigation-launch \
  ros-${ROS_DISTRO}-rviz \
  ttf-droid \
  mesa-dri-intel

CMD roslaunch neonavigation_launch demo.launch
