# slambook (中文说明)

    高翔, 张涛, 颜沁睿, 刘毅, 视觉SLAM十四讲：从理论到实践, 电子工业出版社, 2017
    例程是结合《视觉SLAM十四讲》进行的

# 用到的库说明

    Eigen3 矩阵运算库
    pkg-config --modversion eigen3
    3.3.7

    Pangolin 基于OpenGL的轻量级可视化库,安装的时候，主要先安装Eigen3
    0.3

    Ceres 求解非线性优化问题 依赖Eigen3
    2.0.0

    g2o 图优化库 依赖Eigen3
    20230223

    Sophus 李群李代数库 依赖Eigen3
    
    OpenCV 图像处理库
    pkg-config --modversion opencv4
    4.2.0
    
    DBoW3 词袋模型库
    0.0.1

    gtsam 位姿图优化库 https://gtsam.org/
    dpkg -s libgtsam-dev | grep Version
    4.1.0-1ubuntu2~2224.gbp301d1c

# 目录
## ch2 概述，cmake基础
## ch3 Eigen，三维几何
## ch4 Sophus，李群与李代数
## ch5 OpenCV，图像与相机模型
## ch6 Ceres and g2o，非线性优化
## ch7 特征点法视觉里程计
## ch8 直接法视觉里程计
## ch9 project
## ch10 Ceres and g2o，后端优化1
## ch11 g2o and gtsam，位姿图优化
## ch12 DBoW3，词袋方法
## ch13 稠密地图构建


