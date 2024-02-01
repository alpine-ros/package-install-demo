FROM ghcr.io/alpine-ros/alpine-ros:noetic-3.17-bare

RUN apk add --no-cache \
  ros-${ROS_DISTRO}-neonavigation-launch \
  ros-${ROS_DISTRO}-rviz \
  ttf-droid \
  mesa-dri-gallium

CMD roslaunch neonavigation_launch demo.launch
