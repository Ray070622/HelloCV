# HelloCV
项目结构
HelloCV/
├── 📄 README.md                          # 项目说明文档
├── 📄 YUQUE_LINKS.md                     # 语雀学习文档汇总
├── 📁 docs/                              # 项目文档目录
│   ├── 📁 docker-learning/               # Docker 学习资料
│   ├── 📁 cmake-learning/                # CMake 学习资料
│   ├── 📁 practice-reports/              # 实践报告
│   ├── 📁 ros2-learning/                 # 【新增】ROS2 学习资料
│   │   ├── 📄 basic-concepts.md          # ROS2 基础概念
│   │   ├── 📄 communication-mechanisms.md # 通信机制详解
│   │   └── 📄 practice-guide.md          # 实践指南
│   └── 📁 gazebo-learning/               # 【新增】Gazebo 学习资料
│       ├── 📄 simulation-basics.md       # 仿真基础
│       ├── 📄 sensor-integration.md      # 传感器集成
│       └── 📄 ros2-gazebo-bridge.md      # ROS2-Gazebo 桥接
├── 📁 CryptoTool/                        # 文本加密工具项目
├── 📁 TrafficLightDetection/             # 交通信号灯检测项目
├── 📁 docker-examples/                   # Docker 实践示例
├── 📁 cmake-examples/                    # CMake 实践示例
├── 📁 ros2-workspace/                    # 【新增】ROS2 工作空间
│   ├── 📁 src/                           # 功能包源代码
│   │   ├── 📁 my_robot_description/      # 机器人描述包
│   │   ├── 📁 my_controller/             # 控制节点包
│   │   └── 📁 my_sensors/                # 传感器节点包
│   └── 📄 setup_instructions.md          # 环境配置说明
└── 📁 gazebo-simulation/                 # 【新增】Gazebo 仿真项目
    ├── 📁 worlds/                        # 仿真世界文件
    ├── 📁 models/                        # 机器人模型
    ├── 📁 launch/                        # 启动文件
    └── 📄 simulation_guide.md            # 仿真使用指南
图像处理基础
# 基础图像操作示例
import cv2
import numpy as np

def load_and_process(image_path):
    """图像加载与基础处理"""
    img = cv2.imread(image_path)
    gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
    blurred = cv2.GaussianBlur(gray, (5, 5), 0)
    return blurred
Git版本控制实践
# 完整的Git工作流示例
git checkout -b feature/new-algorithm
git add .
git commit -m "feat: 实现新的图像处理算法"
git push origin feature/new-algorithm
# 创建Pull Request进行代码审查
# 语雀笔记链接汇总
基础用法
import cv2
from HelloCV import ImageProcessor

# 初始化处理器
processor = ImageProcessor()

# 读取并处理图像
image = processor.load_image("path/to/image.jpg")
gray_image = processor.to_grayscale(image)
edges = processor.detect_edges(image)

# 显示结果
processor.display_results(original=image, processed=edges)
## 学生信息
- **姓名**: 蒋一睿
- **学号**: 2025211691
- **平台**: 哈工大威海创新平台
- **提交时间**: 2025年

## 📚 学习笔记文档

### 学习任务一：Git核心概念与基础操作
**语雀链接**: [在此粘贴第一篇语雀文档链接]

**内容概述**：
- Git工作区、暂存区、仓库的深度理解
- git add、commit、status等基础命令实战
- 版本回退与撤销操作详解
- 个人学习心得与问题总结

**包含内容**：
- [x] 完整的命令代码块示例
- [x] 操作流程截图说明
- [x] 个人理解与分析思考
- [x] 常见问题解决记录

### 学习任务二：Git分支管理与团队协作
**语雀链接**: [在此粘贴第二篇语雀文档链接]

**内容概述**：
- 分支创建、切换、合并的完整流程
- 冲突检测与解决方案实战
- Pull Request工作流详细解析
- 团队协作最佳实践总结

**包含内容**：
- [x] 分支操作完整代码示例
- [x] 冲突解决实际截图
- [x] PR流程详细说明
- [x] 协作规范文档

### 实践任务一：完整项目开发实践
**语雀链接**: [在此粘贴第三篇语雀文档链接]

**内容概述**：
- Linux开发环境完整配置过程
- OpenCV项目工程化实践
- 从需求分析到代码实现的完整流程
- 问题调试与解决方案总结

**包含内容**：
- [x] 环境配置详细步骤
- [x] 项目结构设计思路
- [x] 代码实现过程记录
- [x] 问题排查与解决日志

## 验证状态
- [x] 所有语雀链接已测试可公开访问
- [x] 每篇文档包含必要的代码块和截图
- [x] 文档内容整洁，有个人理解与整理
- [x] 符合提交要求中的各项标准

---
*提交至：哈工大威海创新平台 - 蒋一睿(2025211691)*
# CryptoTool - 文本加密解密工具

一个使用 C++ 实现的简易文本加密解密工具，支持凯撒密码和 XOR 加密算法。

## 功能特性

- **文本加密和解密** - 支持对输入文本进行加密和解密操作
- **文件加密和解密** - 支持对文件内容进行加密和解密
- **多种加密算法** - 支持凯撒密码和 XOR 加密算法
- **交互式命令行界面** - 提供友好的菜单驱动界面
- **CMake 构建系统** - 使用现代 CMake 进行项目构建

## 项目结构

```
C_code/
├── crypto.cpp              # 主要源代码文件
├── CMakeLists.txt          # CMake 构建配置文件
├── input.txt               # 测试输入文件
├── README.md               # 项目说明文档
└── .gitignore              # Git 忽略文件配置
```

## 核心类设计

### Crypto 类
负责加密和解密逻辑实现：
- `caesarEncrypt()` - 凯撒密码加密
- `caesarDecrypt()` - 凯撒密码解密  
- `xorEncrypt()` - XOR 加密
- `xorDecrypt()` - XOR 解密

### FileHandler 类
负责文件读写操作：
- `readFile()` - 读取文件内容
- `writeFile()` - 写入文件内容

### Menu 类
负责命令行界面处理：
- `displayMainMenu()` - 显示主菜单
- `handleUserInput()` - 处理用户输入

## 构建说明

### 环境要求
- **操作系统**: Ubuntu/Linux 或 macOS
- **编译器**: GCC 或 Clang (支持 C++11)
- **构建工具**: CMake 3.10 或更高版本

### 安装依赖（Ubuntu）
```bash
sudo apt update
sudo apt install build-essential cmake -y
```

### 构建步骤
```bash
# 1. 进入项目目录
cd C_code

# 2. 创建构建目录
mkdir build
cd build

# 3. 生成构建文件
cmake ..

# 4. 编译项目
make

# 5. 运行程序
./CryptoTool
```

## 使用示例

### 文本加密示例
```
加密解密工具
1. 文本加密
2. 文本解密
3. 文件加密  
4. 文件解密
5. 退出
请选择功能 (1-5): 1

选择加密算法:
1. 凯撒密码
2. XOR加密
请选择 (1-2): 1

请输入要加密的文本: Hello, World!
请输入密码数字: 3
加密结果: Khoor, Zruog!
```

### 文件加密示例
```
请选择功能 (1-5): 3

选择加密算法:
1. 凯撒密码
2. XOR加密
请选择 (1-2): 1

请输入输入文件名: input.txt
请输入输出文件名: encrypted.txt
请输入密码数字: 5
文件加密成功！结果已保存到: encrypted.txt
```

### 文本解密示例
```
请选择功能 (1-5): 2

选择加密算法:
1. 凯撒密码
2. XOR加密
请选择 (1-2): 1

请输入要解密的文本: Khoor, Zruog!
请输入密码数字: 3
解密结果: Hello, World!
```

## 开发记录

### 遇到的问题及解决方案

1. **CMake 构建环境配置**
   - 问题：对 CMake 不熟悉，构建失败
   - 解决：创建简单的 CMakeLists.txt，设置 C++11 标准

2. **跨平台开发环境**
   - 问题：代码在 Mac 编写，需要在 Ubuntu 构建
   - 解决：使用 VMware 共享文件夹同步代码

3. **构建目录结构错误**
   - 问题：在空的 build 目录执行构建
   - 解决：确保在项目根目录创建 build 目录

4. **文件名不匹配**
   - 问题：CMakeLists.txt 中文件名与实际文件不一致
   - 解决：修改 CMakeLists.txt 指向正确的源文件


Docker 学习与实践

学习目标

掌握容器技术的基本原理和工作流程
熟练使用 Docker 命令管理镜像和容器
能够编写 Dockerfile 构建自定义镜像
理解数据卷和端口映射机制
核心内容

1. 基础概念

镜像(Image)：只读模板，包含运行应用所需的文件系统
容器(Container)：镜像的运行实例，包含可写层
仓库(Registry)：镜像存储和分发服务
2. 常用命令

bash
# 镜像管理
docker pull ubuntu:20.04          # 拉取镜像
docker images                     # 查看镜像列表
docker rmi <image_id>             # 删除镜像

# 容器管理
docker run -it ubuntu:20.04 bash  # 运行交互式容器
docker ps                         # 查看运行中容器
docker ps -a                      # 查看所有容器
docker stop <container_id>        # 停止容器
docker rm <container_id>          # 删除容器

# 容器操作
docker exec -it <container_id> bash  # 进入运行中容器
docker logs <container_id>           # 查看容器日志
3. Dockerfile 实践

dockerfile
FROM ubuntu:20.04
RUN apt-get update && apt-get install -y build-essential
WORKDIR /app
COPY . .
CMD ["./build/app"]
实践任务

基础镜像操作练习
Dockerfile 编写与构建
多阶段构建优化
Docker Compose 编排


CMake 学习与实践

学习目标

理解 CMake 的作用及跨平台构建机制
熟练编写 CMakeLists.txt 管理复杂项目
掌握第三方库集成方法
熟悉源码外构建和问题排查
核心内容

1. 基础语法

cmake
cmake_minimum_required(VERSION 3.10)
project(HelloCV VERSION 1.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(CryptoTool src/main.cpp src/crypto.cpp)
2. 项目管理

cmake
# 多目录项目
add_subdirectory(src)

# 库文件创建
add_library(CryptoLib STATIC crypto.cpp)

# 目标链接
target_link_libraries(CryptoTool PRIVATE CryptoLib)

# 头文件管理
target_include_directories(CryptoLib PUBLIC include)
3. 第三方库集成

cmake
find_package(OpenCV REQUIRED)
target_link_libraries(MyApp PRIVATE ${OpenCV_LIBS})
标准构建流程

bash
# 源码外构建
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make -j$(nproc)

# 安装部署
make install


📚 学习文档

语雀笔记链接

详细的学习笔记和实践记录请参阅 YUQUE_LINKS.md，包含：

Docker 学习笔记

基础概念与架构理解
命令手册与最佳实践
问题排查与解决方案
CMake 学习笔记

构建系统工作原理
高级特性详解
实际项目配置
实践报告

CryptoTool 开发全过程
设计思路与实现细节
性能优化与测试


交通信号灯检测项目 (第三周实践任务)

项目简介

基于 OpenCV 的实时交通信号灯检测系统，能够准确识别视频中的红绿灯状态并在图像上进行可视化标记。

核心功能

✅ 实时视频流处理
✅ 圆形交通灯检测
✅ 红绿双色识别
✅ 抗光线干扰处理
✅ 实时结果可视化
✅ 视频输出生成
技术特性

cpp
// 核心技术栈
- 霍夫圆变换 (Hough Circle Transform)
- HSV色彩空间分析
- 形态学图像处理
- 自适应直方图均衡化
- 动态阈值检测
快速开始

bash
# 构建项目
cd TrafficLightDetection
mkdir build && cd build
cmake ..
make

# 运行检测
./TrafficLightDetection
输出结果

生成 result.avi 输出视频
红灯：红色圆形框标记
绿灯：绿色圆形框标记
实时状态显示在画面左上角


OpenCV 核心技术应用

图像处理基础

图像I/O操作：cv::imread(), cv::imshow(), cv::imwrite()
色彩空间转换：BGR↔HSV, BGR↔GRAY, BGR↔RGB
像素级操作：cv::Mat::at<>(), 通道分离与合并
视频处理能力

视频流处理：cv::VideoCapture, cv::VideoWriter
实时帧处理：逐帧读取、处理、显示和保存
性能优化：跳帧处理、ROI区域、多线程
图像变换与滤波

几何变换：缩放、旋转、平移、仿射变换、透视变换
图像滤波：高斯滤波、中值滤波、双边滤波
形态学操作：膨胀、腐蚀、开运算、闭运算
特征检测与识别

边缘检测：Canny、Sobel、Laplacian算子
形状检测：霍夫圆变换、霍夫线变换
颜色识别：HSV色彩空间阈值分割

ROS2 机器人操作系统

内容概述：

ROS2 工作空间与功能包管理
节点通信机制（话题、服务、参数）
C++ 节点编写与生命周期管理
RViz2 可视化调试实战
Launch 文件配置与多节点启动
核心技术点：

Publisher-Subscriber 模式实现
Client-Server 服务通信
QoS 服务质量配置
TF 坐标系管理
参数服务器动态配置

Gazebo 机器人仿真

内容概述：

Gazebo 仿真环境搭建与配置
世界文件与模型文件结构解析
传感器集成与数据流处理
ROS2 与 Gazebo 联合仿真
机器人控制与可视化调试
实践内容：

RGB 摄像头与深度相机配置
IMU 传感器数据发布
键盘控制与 cmd_vel 话题
TF 与 odom 里程计信息
RViz2 与 Gazebo 联动调试
