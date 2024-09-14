cmake_minimum_required(VERSION 3.27)
project(slambook)
# Eigen3
include_directories("/usr/include/eigen3")
# 添加Pangolin依赖
find_package(Pangolin REQUIRED)
include_directories(${Pangolin_INCLUDE_DIRS})
message(STATUS "Pangolin_INCLUDE_DIRS: ${Pangolin_INCLUDE_DIRS}")
# 为使用 sophus，您需要使用find_package命令找到它
find_package(Sophus REQUIRED)
set(Sophus_LIBRARIES Sophus)
# 未添加Sophus头文件路径的原因是源文件cmakelist.txt中 27 28 设置的路径不是安装路径
#include_directories(${Sophus_INCLUDE_DIRS})
# 寻找OpenCV库
find_package(OpenCV REQUIRED)
# pcl
find_package(PCL REQUIRED COMPONENT common io filters)
include_directories(${PCL_INCLUDE_DIRS})
add_definitions(${PCL_DEFINITIONS})
# 寻找Ceres库并添加它的头文件
find_package(Ceres REQUIRED)
include_directories(${CERES_INCLUDE_DIRS})
# 寻找G2O 没有用G2O下的cmake_modules
#find_package(G2O REQUIRED)
#include_directories(${G2O_INCLUDE_DIRS})
# CSparse 由于没有用G2O下的cmake_modules
#find_package(CSparse REQUIRED)
#include_directories(${CSPARSE_INCLUDE_DIR})
# Cholmod 由于没有用G2O下的cmake_modules
#Find_Package(Cholmod REQUIRED)
#include_directories(${CHOLMOD_INCLUDE_DIR})
# gtsam
find_package(GTSAMCMakeTools)
find_package(GTSAM REQUIRED)
include_directories(${GTSAM_INCLUDE_DIR})
# DBoW3
set(DBoW3_LIBS DBoW3)

# octomap
find_package(octomap REQUIRED)
include_directories(${OCTOMAP_INCLUDE_DIRS})

##ch2
add_subdirectory(ch2)
#ch3
add_subdirectory(ch3)
#ch4
add_subdirectory(ch4)
#ch5
add_subdirectory(ch5)
#ch6
add_subdirectory(ch6)
#ch7
add_subdirectory(ch7)
#ch8
add_subdirectory(ch8)
#ch10
add_subdirectory(ch10)
#ch11
add_subdirectory(ch11)
#ch12
add_subdirectory(ch12)
#ch13
add_subdirectory(ch13)

add_subdirectory(project/0.1)
add_subdirectory(project/0.2)
add_subdirectory(project/0.3)
add_subdirectory(project/0.4)