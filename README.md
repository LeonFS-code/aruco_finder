# aruco_finder

## Camera Calibration
This part is based in the [site](http://wiki.ros.org/camera_calibration/Tutorials/MonocularCalibration) /
To install the code to calibrate a monocular camera
```
rosdep install camera_calibration
```
To run this code 
```
rosrun camera_calibration cameracalibrator.py --size 8x6 --square 0.108 image:=/usb_cam/image_raw camera:=/usb_cam  --no-service-check
```
## Webcan
This part is based in the [site](http://ros-developer.com/2017/04/23/aruco-ros/)
To start publishing images
```
roslaunch aruco_finder usb_cam_stream_publisher.launch
```
To find the marker
```
roslaunch aruco_marker_finder.launch markerId:=701 markerSize:=0.05
```
To see the images
```
rosrun rqt_image_view rqt_image_view
```