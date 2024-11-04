Camera Calibration Rolling but Foxy Compatible
==============
1. BUILD JUST THE CAMERA CALIBRATION PACKAGE 
`colcon build --packages-select camera_calibration`
2. Install [pyenv](https://github.com/pyenv/pyenv) in order to use Python 3.10
   
   2.1. `curl https://pyenv.run | bash `
   
   2.2.  nano ~/.bashrc
   
   2.3 Add the following lines at the end of the file:
   ```bash

   export PATH="$HOME/.pyenv/bin:$PATH"
   eval "$(pyenv init --path)"
   eval "$(pyenv init -)"
   ```
   2.4. `pyenv install 3.10.4`

   2.5 `pyenv local 3.10.4`
3. Follow the instruction for the camera calibration
`ros2 run camera_calibration cameracalibrator ros2 run camera_calibration cameracalibrator --size 8x6 --square 0.108 image:=/front/image camera:=/camera
`


image_pipeline
==============

[![Build Status](https://build.ros2.org/buildStatus/icon?job=Rdev__image_pipeline__ubuntu_noble_amd64)](https://build.ros2.org/job/Rdev__image_pipeline__ubuntu_noble_amd64/)

This package fills the gap between getting raw images from a camera driver and higher-level vision processing.

Documentation is hosted in the ROS 2 API docs.
The [image_pipeline](http://docs.ros.org/en/rolling/p/image_pipeline/)
documentation includes an overview,
[details on camera_info](http://docs.ros.org/en/rolling/p/image_pipeline/camera_info.html),
and links to the documentation for each individual package.

Not every aspect has been ported to the new ROS 2 API documentation yet, so
there is still additional (partially outdated) information
in [the ROS wiki entry](http://wiki.ros.org/image_pipeline).

If you are using an Nvidia Jetson platform, consider using modules from [Isaac Image Proc](https://github.com/NVIDIA-ISAAC-ROS/isaac_ros_image_pipeline) - a collection of hardware accelerated `image_proc` features for the Jetsons.
