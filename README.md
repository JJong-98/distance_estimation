# distance_estimation

1. catkin_make해서 예선 폴더의 yolo_usbcam.py의 darknet_ros msg가 잘 import 되었는지 확인
   - 모듈 없다고 err뜨면
  catkin_make -DCATKIN_WHITELIST_PACKAGES=“darknet;darknet_ros;darknet_ros_msgs”  -DCMAKE_BUILD_TYPE=Release
   
   
2. calibration 된 카메라 토픽을 sub하게 되어있어서
    roslaunch usb_cam usb_cam_calib.launch
   
   
3. darknet_ros 폴더에서 협로 주행에 맞게 cfg, weight(드라이브), yaml 수정
   - 이때도 calibration 카메라 토픽으로 바꿈
    roslaunch darknet_ros darknet_ros.launch
   
   
4. python yolo_usbcam.py


