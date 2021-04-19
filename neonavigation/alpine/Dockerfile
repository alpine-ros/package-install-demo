FROM ghcr.io/alpine-ros/alpine-ros:noetic-bare

RUN apk add --no-cache \
  ros-${ROS_DISTRO}-neonavigation-launch \
  ros-${ROS_DISTRO}-rviz

# Setup GUI related configs to run from container
RUN apk add --no-cache dbus ttf-droid mesa-dri-intel \
  && dbus-uuidgen \
  && apk del --no-cache dbus \
  && mkdir /usr/share/X11/xkb

CMD roslaunch neonavigation_launch demo.launch
