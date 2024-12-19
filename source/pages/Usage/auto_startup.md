# HCX 机器人 驱动自启服务

```{toctree}
:maxdepth: 1
:glob:
```

```{contents} Contents
:depth: 2
:local:
```

## 使用方法

### 开启驱动自启服务

```
systemctl start diablo_startup.service # 立即开启驱动自启服务
```

### 查看驱动自启服务状态

```
systemctl status diablo_startup.service # 查看驱动自启服务状态
```

### 重启驱动自启服务

```
systemctl restart diablo_startup.service # 重启驱动自启服务
```

### 停止驱动自启服务
```
systemctl stop diablo_startup.service  # 停止驱动自启服务
```

### 启动自启服务
```
systemctl enable diablo_startup.service  # 开启开机驱动自启服务
```

### 禁用自启服务

```
systemctl disable diablo_startup.service # 禁止开机驱动自启服务
```