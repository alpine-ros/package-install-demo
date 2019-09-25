FROM alpineros/alpine-ros:melodic-ros-core

RUN apk add --no-cache \
  ros-${ROS_DISTRO}-neonavigation-launch \
  ros-${ROS_DISTRO}-rviz

# Setup GUI related configs to run from container
# コンテナ内からGUIを正しく表示するためのおまじない
RUN apk add --no-cache dbus font-noto mesa-dri-intel \
  && dbus-uuidgen \
  && apk del --no-cache dbus \
  && mkdir /usr/share/X11/xkb
COPY 00-font.conf /etc/fonts/conf.d/

CMD roslaunch neonavigation_launch demo.launch
