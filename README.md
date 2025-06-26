For building install protobuf, robot state publisher and dependecies:

```
sudo apt-get install -y python-wstool python-rosdep ninja-build stow

cd carto_ws

wstool update -t src
src/cartographer/scripts/install_proto3.sh
sudo rosdep init   
rosdep update

rosdep install --from-paths src --ignore-src --rosdistro=${ROS_DISTRO} -y
cd carto_ws/src
git clone https://github.com/GT-RAIL/robot_pose_publisher.git
```
For detailed instructions, 
https://github.com/snktshrma/Ardupilot-Cartographer-SLAM
https://ardupilot.org/dev/docs/ros-cartographer-slam.html

