# HelloCV
项目结构
HelloCV/
├── 📄 README.md                          # 项目说明文档
├── 📄 YUQUE_LINKS.md                     # 语雀学习文档汇总
├── 📁 docs/                              # 项目文档目录
│   ├── 📁 docker-learning/               # Docker 学习资料
│   │   ├── 📄 basic-concepts.md          # 基础概念笔记
│   │   ├── 📄 commands-handbook.md       # 命令手册
│   │   └── 📄 practice-records.md        # 实践记录
│   ├── 📁 cmake-learning/                # CMake 学习资料
│   │   ├── 📄 cmake-introduction.md      # CMake 介绍
│   │   ├── 📄 advanced-features.md       # 高级特性
│   │   └── 📄 troubleshooting.md         # 问题排查
│   └── 📁 practice-reports/              # 实践报告
│       └── 📄 cryptotool-development.md  # 加密工具开发报告
├── 📁 CryptoTool/                        # 文本加密工具项目
│   ├── 📄 CMakeLists.txt                 # 项目构建配置
│   ├── 📁 src/                           # 源代码目录
│   │   ├── 📄 main.cpp                   # 主程序入口
│   │   ├── 📄 crypto.cpp                 # 加密算法实现
│   │   ├── 📄 crypto.h                   # 加密算法头文件
│   │   ├── 📄 file_handler.cpp           # 文件处理实现
│   │   ├── 📄 file_handler.h             # 文件处理头文件
│   │   ├── 📄 menu.cpp                   # 用户界面实现
│   │   └── 📄 menu.h                     # 用户界面头文件
│   ├── 📁 include/                       # 头文件目录
│   └── 📁 build/                         # 构建输出目录
├── 📁 docker-examples/                   # Docker 实践示例
│   ├── 📄 Dockerfile                     # 基础 Dockerfile
│   ├── 📄 docker-compose.yml             # 容器编排配置
│   └── 📁 practice-scripts/              # 练习脚本
├── 📁 cmake-examples/                    # CMake 实践示例
│   ├── 📄 basic-example/                 # 基础示例
│   ├── 📄 multi-directory/               # 多目录项目
│   └── 📄 thirdparty-integration/        # 第三方库集成
└── 📄 requirements.txt                   # Python 依赖列表（可选）
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


