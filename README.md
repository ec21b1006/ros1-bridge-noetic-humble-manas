# Ros1-bridge for noetic & humble
- You can follow the same [Installation of Humble from source](https://docs.ros.org/en/humble/Installation/Alternatives/Ubuntu-Development-Setup.html)
- Donot unsource ros1 noetic until you reach to the step of `rosdep install --from-paths src --ignore-src -y --skip-keys "fastcdr rti-connext-dds-6.0.1 urdfdom_headers"`
- During `sudo rosdep init` it will show website may be down. You can directly turn on/off any vpn or check your internet connection.
- During colcon building the ros1_bridge keep in mind to clone the ros1_bridge git to some where and then go inside that ros1_bridge which you have cloned and then do the colcon build with ros1_bridge {make sure to source both ros1 and ros2}


## If you are building noetic from source in the ros 2 container and building the rosbridge there itself
- during `sudo apt-get install python3-rosdep python3-rosinstall-generator python3-vcstools python3-vcstool build-essential` you will get a lot of errors. Just do `sudo apt clean && sudo apt update`.
- during `rosdep updates` you will get some errors. At this point just turn off/on your vpn.
- during `rosdep install --from-paths ./src --ignore-packages-from-source --rosdistro noetic -y` you will get an error of hddtemp not available for ubuntu 22.04. You can do `export ROS_OS_OVERRIDE=ubuntu:20.04:focal`
- 
