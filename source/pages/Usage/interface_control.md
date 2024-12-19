# HCX 机器人外设控制

```{toctree}
:maxdepth: 1
:glob:
```

```{contents} Contents
:depth: 2
:local:
```

这里的外设控制指的是控制 HCX 机器人的探照灯和氛围灯。

## 探照灯控制

## 打开探照灯

```
ros2 topic pub /led std_msgs/msg/String "{data: 0 255 0 0}" --once
```

## 关闭探照灯

```
ros2 topic pub /led std_msgs/msg/String "{data: 0 0 0 0}" --once
```
## 氛围灯控制

氛围灯为 HCX 机器人前脸上的 LED 灯带，用于装饰和氛围营造。

假设你正好站在机器人的正后方，氛围灯的序号对应从右到左依次为 `1-3`。

![](../../_static/led.jpg)

### 打开右氛围灯

```
ros2 topic pub /led std_msgs/msg/String "{data: 1 255 0 0}" --once
```

### 关闭右氛围灯

```
ros2 topic pub /led std_msgs/msg/String "{data: 1 0 0 0}" --once
```

### 打开中间氛围灯

```
ros2 topic pub /led std_msgs/msg/String "{data: 2 255 0 0}" --once
```

### 关闭中间氛围灯

```
ros2 topic pub /led std_msgs/msg/String "{data: 2 0 0 0}" --once
```

### 打开左氛围灯

```
ros2 topic pub /led std_msgs/msg/String "{data: 3 255 0 0}" --once
```

### 关闭左氛围灯

```
ros2 topic pub /led std_msgs/msg/String "{data: 3 0 0 0}" --once
```