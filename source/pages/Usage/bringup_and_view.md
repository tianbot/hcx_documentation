# 启动整机驱动和可视化传感器数据

```{toctree}
:maxdepth: 1
:glob:
```

```{contents} Contents
:depth: 2
:local:
```

## 启动整机 ROS 驱动

- 启动底盘驱动
- 启动传感器驱动
- 启动外设驱动

```bash
ros2 launch diablo_bringup diablo_bringup.launch.py
```

## 在 rviz 中查看传感器数据

### 1. 启动 rviz
```bash
ros2 launch diablo_rviz view_robot.launch.py 
```

```{note}
这一步需要先启动机器人，否则rviz无法获取传感器数据
```

### 2. 查看机器人状态
点击左侧导航栏的“可视化”按钮，进入可视化界面，可以看到当前机器人所连接的传感器数据。

![可视化界面](../../_static/view_robot_and_sensor.png)

