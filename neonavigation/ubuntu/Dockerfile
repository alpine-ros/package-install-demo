FROM ros:melodic-ros-core

# 国内のリポジトリを利用するように変更
RUN sed -e \
  's|http://archive.ubuntu.com|http://linux.yz.yamagata-u.ac.jp/ubuntu|' \
  -i /etc/apt/sources.list

# パッケージインストール
RUN apt-get update -qq \
  && apt-get install -y --no-install-recommends \
    ros-${ROS_DISTRO}-neonavigation-launch \
    ros-${ROS_DISTRO}-rviz \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*

# コンテナ内からGUIを正しく表示するためのおまじない
RUN apt-get update -qq \
  && apt-get install -y --no-install-recommends dbus \
  && dbus-uuidgen \
  && apt-get purge -y dbus \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*

CMD roslaunch neonavigation_launch demo.launch
