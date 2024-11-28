# 用户接口 (ros 端)

```{toctree}
:maxdepth: 1
:glob:
```

```{contents} Contents
:depth: 2
:local:
```

## 用户控制接口

以下是用户接口，用户可以向这些 ROS 话题接口发布消息，以控制机器人外设和运动状态

| 外设接口名称 | 话题名称 | 话题类型/发布者数量 | 发布频率 |  
| :---: | :---: | :---: | :---: |
|    mqtt 接口    |  /mqtt_txd   | [std_msgs/msg/String]    | 10hz   |
|    速度控制接口  |  /cmd_vel    | [geometry_msgs/msg/Twist] | 10hz  |
|    站立控制接口  |  /stand      | [std_msgs/msg/String]     | 10hz  |
~~|    键盘控制接口  |  /key_control | [motion_msgs/msg/MotionCtrl]    | 10hz  |~~
~~|  MotionCmd 运动接口 | /diablo/MotionCmd |  [motion_msgs/msg/MotionCtrl]   |10hz |~~
|     照明灯接口  | /illumination_led_color |   [std_msgs/msg/ColorRGBA]     |  10hz  |
|     氛围灯      | /led              | [std_msgs/msg/String]     |  10hz  | 
|     左氛围灯    | /left_led_color    | [std_msgs/msg/ColorRGBA]  |  10hz  |
|     中氛围灯    | /middle_led_color  | [std_msgs/msg/ColorRGBA]  |  10hz  |
|     右氛围灯    | /right_led_color   | [std_msgs/msg/ColorRGBA]  |  10hz  |

## /mqtt_txd 接口说明

|  字段 | 类型   | 描述 | 机器人状态 |
| :---: | :---: | :---: | :---: |
| data | string |  `setled led_num r g b `          |  控制探照灯、f 氛围灯  |   用户视角（上行） |
| data | string |  `setvel linear_vel angular_vel`  |  控制机器人运动       |    用户视角（上行） |
| data | string |  `setpose num`  | num  控制 z 位置的状态值，1：站起，0：蹲下 |    用户视角（上行） |
| data | string |  `BATT xxxV`    |  向 mqtt 以 10hz 持续返回电池电量        |    用户视角（下行） |

### /led 接口说明

|  字段 | 类型   | 描述 | 机器人状态 |
| :---: | :---: | :---: | :---: |
| data | string |  `0 r g b`     |  开启探照灯 |
| data | string |  `0 0 0 0 `    |  关闭探照灯 |
| data | string |  `1 r g b`     |  控制右侧氛围灯，x x x 依次为 rgb 的值 |
| data | string |  `1 0 0 0 `    |  关闭右侧氛围灯 |
| data | string |  `2 r g b`     |  控制中间氛围灯，x x x 依次为 rgb 的值 |
| data | string |  `2 0 0 0 `    |  关闭中间氛围灯 |
| data | string |  `3 r g b`     |  控制左侧氛围灯，x x x 依次为 rgb 的值 |
| data | string |  `3 0 0 0 `    |  关闭左侧氛围灯 |

### /Stand 接口说明

| 字段 | 类型 | 描述 | 机器人状态 |
| :---: | :---: | :---: | :---: |
| data | string |  `standup` |  站立 |
| data | string |  `sitdown` |  坐下 |
| data | string |  `其他 string` |  保持状态 |
