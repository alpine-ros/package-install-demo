FROM ros:noetic-ros-core

# Use fastest mirror in Japan (for ROSCon JP live demo)
# 国内のリポジトリを利用するように変更
# RUN sed -e \
#   's|http://archive.ubuntu.com|http://linux.yz.yamagata-u.ac.jp/ubuntu|' \
#   -i /etc/apt/sources.list

RUN apt-get update -qq \
  && apt-get install -y --no-install-recommends \
    ros-${ROS_DISTRO}-neonavigation-launch \
    ros-${ROS_DISTRO}-rviz \
    dbus \
  && dbus-uuidgen \
  && apt-get purge -y dbus \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*

CMD roslaunch neonavigation_launch demo.launch
