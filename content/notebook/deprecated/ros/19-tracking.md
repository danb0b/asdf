---
title: CV Bridge and Python 3
weight: 190
tags:
- ros
- ubuntu
- linux
- camera
- opencv
summary: " "
---
getting cv_bridge working with python 3 is less straightforward.  you need to recompile cv_bridge locally.

```bash
git clone https://github.com/idealabasu/vision_opencv.git
cd vision_opencv
git checkout melodic
cp -r cv_bridge/ ../code_idealab_ros/src
cp -r image_geometry/ ../code_idealab_ros/src
cp -r vision_opencv/ ../code_idealab_ros/src
cd ~/code/code_idealab_ros/
catkin_make -DPYTHON_EXECUTABLE=/usr/bin/python3
```

1. install imutils
pip3 install imutils

1. run ros

    in one terminal
    ```
    roscore
    ```

    in second terminal
    ```
    rosrun libuvc_camera camera_node
    ```

    in third terminal
    ```
    rosrun tracking tracker.py
    ```
