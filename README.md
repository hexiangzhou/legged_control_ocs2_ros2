# legged_control_ocs2


## Introduction


## Installation
### Prerequisites
* Ubuntu 22.04
* ros2 humble
* C++ compiler with C++17 support
* Eigen (v3.4)
* Boost C++ (v1.74)

### Source code
```
# Clone legged_control
git clone https://github.com/hexiangzhou/legged_control_ocs2.git
```

### OCS2_ROS2
The ocs2_ros2 library is based on [zhengxiang94/ocs2_ros2](https://github.com/zhengxiang94/ocs2_ros2.git)
```
# Clone ocs2_ros2 in ros2_ws/src/legged_control_ocs2
cd ~/ros2_ws/src/legged_control_ocs2
# Clone ocs2_ros2
git clone https://github.com/zhengxiang94/ocs2_ros2.git
# Clone pinocchio
git clone --recurse-submodules https://github.com/zhengxiang94/pinocchio.git
# Clone hpp-fcl
git clone --recurse-submodules https://github.com/zhengxiang94/hpp-fcl.git
# Clone ocs2_robotic_assets
git clone https://github.com/zhengxiang94/ocs2_robotic_assets.git
# Clone plane_segmentation_ros2
git clone https://github.com/zhengxiang94/plane_segmentation_ros2.git
```

### Others
```
# Install dependencies
sudo apt-get install ros-iron-grid-map-cv ros-iron-grid-map-msgs ros-iron-grid-map-ros ros-iron-grid-map-sdf libmpfr-dev libpcap-dev libglpk-dev
sudo apt install ros-humble-octomap
```

## Build
### Build ocs2
```
# Debug: If downloading the dependencies via HTTPS fails, use SSH instead
git config --global url."git@github.com:".insteadOf https://github.com/
colcon build --packages-up-to ocs2_legged_robot_ros ocs2_self_collision_visualization --cmake-args -DCMAKE_BUILD_TYPE=RelWithDebInfo
```


