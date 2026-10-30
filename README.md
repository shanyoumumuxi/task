# 任务提交

## 目录结构

```text
.
├── task1
│   └── environment
│       ├── 1-ubuntu-version.png
│       ├── 2-apt-update.png
│       ├── 3-github-curl.png
│       ├── 4-github-login.png
│       └── 6-cpp-env.png
├── task2
│   ├── cpp
│   │   ├── 1
│   │   │   ├── 1.png
│   │   │   ├── 2.png
│   │   │   ├── 3.png
│   │   │   ├── 4.png
│   │   │   ├── 5.png
│   │   │   └── code.md
│   │   └── 2
│   │       ├── 1.png
│   │       ├── 2.png
│   │       ├── 3.png
│   │       ├── 4.png
│   │       ├── 5.png
│   │       └── code.md
│   └── ros
│       ├── keyboard-control.png
│       └── turtlesim-result.png
├── task3
│   ├── cpp
│   │   ├── 3
│   │   │   ├── 1.png
│   │   │   ├── 2.png
│   │   │   ├── 3.png
│   │   │   ├── 4.png
│   │   │   ├── 5.png
│   │   │   └── code.md
│   │   └── 4
│   │       ├── 1.png
│   │       ├── 2.png
│   │       ├── 3.png
│   │       ├── 4.png
│   │       ├── 5.png
│   │       └── code.md
│   └── ros
│       └── helloworld-result.png
├── task4
│   └── cpp
│       └── 6
│           ├── 1.png
│           ├── 2.png
│           ├── 3.png
│           ├── 4.png
│           ├── 5.png
│           └── code.md
├── task5
│   └── ros
│       └── topic
│           ├── item-publisher.png
│           └── item-subscriber.png
└── README.md
```

## 任务说明

### 第一次任务

1. 相关环境配置
   - Ubuntu 22.04.5 LTS 虚拟机环境
   - C++ 环境配置
   - 截图：`task1/environment/`
2. 熟悉 git 简单操作

### 第二次任务

1. 学习 C++ 基础语法，在洛谷题单广场「入门1」「入门2」中各完成 5 题
   - 代码：`task2/cpp/1/code.md`、`task2/cpp/2/code.md`
   - 运行结果截图：`task2/cpp/1/1.png` 至 `5.png`、`task2/cpp/2/1.png` 至 `5.png`
2. 配置 ROS 2 环境，实现键盘控制小海龟
   - 截图：`task2/ros/`

### 第三次任务

1. 继续学习 C++ 基础语法，在洛谷题单广场「入门3」「入门4」中各完成 5 题
   - 代码：`task3/cpp/3/code.md`、`task3/cpp/4/code.md`
   - 评测结果截图：`task3/cpp/3/1.png` 至 `5.png`、`task3/cpp/4/1.png` 至 `5.png`
2. 学习 ROS 2 节点，运行 C++ 节点输出 helloworld
   - 运行截图：`task3/ros/helloworld-result.png`

### 第四次任务

1. 继续学习 C++ 基础语法，完成“洛谷题6”中的 5 道题
   - 代码：`task4/cpp/6/code.md`
   - 评测结果截图：`task4/cpp/6/1.png` 至 `5.png`

### 第五次任务

1. 学习 ROS 2 话题与自定义消息，用 C++ 发布、接收并打印物品信息
   - 物品信息：ID `1001`、名称 `Apple`、描述 `Fresh fruit`、价格 `3.50`
   - 发布者运行截图：`task5/ros/topic/item-publisher.png`
   - 订阅者运行截图：`task5/ros/topic/item-subscriber.png`
   - 两端输出中的物品 ID 和基本信息一致
2. 服务与自定义服务接口：服务端和客户端交替输出斐波那契数列，运行材料待补充
3. 动作与自定义动作接口：累加 1 至 N，显示反馈及最终结果，运行材料待补充
