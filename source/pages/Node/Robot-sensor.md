# 传感器 (ros 端)

```{toctree}
:maxdepth: 1
:glob:
```

```{contents} Contents
:depth: 2
:local:
```

## 传感器数据源接口

以下是用户传感器接口，用户可以订阅这些 ROS 话题接口接受消息，以控制机器人传感器数据

| 传感器名称 | 话题名称 | 话题类型/发布者数量 | 发布频率 |
| :---: | :---: | :---: | :---: |
| RGB-D 相机 | /camera/color/camera_info           | [sensor_msgs/msg/CameraInfo] 1 publisher            |15hz     |
| RGB-D 相机 | /camera/color/image_raw     | [sensor_msgs/msg/Image] 1 publisher |15hz     |
| RGB-D 相机 | /camera/color/metadata      | [realsense2_camera_msgs/msg/Metadata] 1 publisher   |15hz     |
| RGB-D 相机 | /camera/depth/camera_info   | [sensor_msgs/msg/CameraInfo] 1 publisher    |15hz     |
| RGB-D 相机 | /camera/depth/image_rect_raw| [sensor_msgs/msg/Image] 1 publisher |15hz     |
| RGB-D 相机 | /camera/depth/metadata      | [realsense2_camera_msgs/msg/Metadata] 1 publisher   |15hz     |
| RGB-D 相机 | /camera/extrinsics/depth_to_color   | [realsense2_camera_msgs/msg/Extrinsics] 1 publisher | |
| RGB-D 相机 | /camera/extrinsics/depth_to_depth   | [realsense2_camera_msgs/msg/Extrinsics] 1 publisher | |
| RGB-D 相机 | /camera/imu       | [sensor_msgs/msg/Imu] 1 publisher      ||
| 底盘电池电压 | /diablo/sensor/Battery    | [sensor_msgs/msg/BatteryState] 1 publisher     |    2hz|
| 底盘状态    | /diablo/sensor/Body_state | [motion_msgs/msg/RobotStatus] 1 publisher      |   10hz|
| 底盘 imu    | /diablo/sensor/Imu| [sensor_msgs/msg/Imu] 1 publisher      |   30hz|
| 底盘电池电压 | /diablo/sensor/ImuEuler   | [ception_msgs/msg/IMUEuler] 1 publisher|    满电电压 42v    30hz|
| 底盘电机状态 | /diablo/sensor/Motors | [motion_msgs/msg/LegMotors] 1 publisher    |   30hz|
| 运动学底盘轮式里程计 | /diablo_odom  | [nav_msgs/msg/Odometry] 1 publisher      |   30hz|
|            | /diagnostics  | [diagnostic_msgs/msg/DiagnosticArray] 1 publisher       |    2hz|
| 底盘电池电压 | /joint_states | [sensor_msgs/msg/JointState] 1 publisher   |     10hz |
| 多线激光雷达 | /livox/imu    | [sensor_msgs/msg/Imu] 1 publisher  |  200hz|
| 多线激光雷达 | /livox/lidar  | [sensor_msgs/msg/PointCloud2] 1 publisher  |  10hz |
| mqtt 话题接受端 | /mqtt_rxd  | [std_msgs/msg/String] 1 publisher  |   3hz |
| mqtt 话题发送端 | /mqtt_txd  | [std_msgs/msg/String] 1 publisher  |   3hz |
| ekf 底盘轮式里程计 | /odom         | [nav_msgs/msg/Odometry] 1 publisher|  20hz |
|                | /parameter_events     | [rcl_interfaces/msg/ParameterEvent] 20 publishers  |       |
| 机器人 urdf 描述 | /robot_description    | [std_msgs/msg/String] 1 publisher      |           |
|                | /rosout   |  [rcl_interfaces/msg/Log] 22 publishers        |       3hz |
|  2D 激光雷达    | /scan     | [sensor_msgs/msg/LaserScan] 1 publisher         |      10hz |
| 关键部件的坐标变换关系         |  /tf          | [tf2_msgs/msg/TFMessage]    2 publishers       |      30hz |
| 关键部件的坐标变换关系         | /tf_static    |  [tf2_msgs/msg/TFMessage]      |   |