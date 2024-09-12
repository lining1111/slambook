cmake_minimum_required(VERSION 3.27)
project(slambook)
# Eigen3
find_package(Eigen3 REQUIRED)
include_directories(${Eigen3_INCLUDE_DIRS})
# 添加Pangolin依赖
find_package(Pangolin REQUIRED)
include_directories(${Pangolin_INCLUDE_DIRS})
# 为使用 sophus，您需要使用find_package命令找到它
find_package(Sophus REQUIRED)
#include_directories(${Sophus_INCLUDE_DIRS})
#message(STATUS "Sophus_INCLUDE_DIRS = ${Sophus_INCLUDE_DIRS}")
# 寻找OpenCV库
find_package(OpenCV 4 REQUIRED)
# pcl
find_package(PCL REQUIRED COMPONENT common io)
include_directories(${PCL_INCLUDE_DIRS})
add_definitions(${PCL_DEFINITIONS})
# 寻找Ceres库并添加它的头文件
find_package(Ceres REQUIRED)
include_directories(${CERES_INCLUDE_DIRS})
# 寻找G2O
#find_package(G2O REQUIRED)
#include_directories(${G2O_INCLUDE_DIRS})
# CSparse
#find_package(CSparse REQUIRED)
#include_directories(${CSPARSE_INCLUDE_DIR})
#Cholmod
#Find_Package(Cholmod REQUIRED)
#include_directories(${CHOLMOD_INCLUDE_DIR})
# gtsam
find_package( GTSAMCMakeTools )
find_package( GTSAM REQUIRED )
include_directories( ${GTSAM_INCLUDE_DIR} )
# octomap
find_package( octomap REQUIRED )
include_directories( ${OCTOMAP_INCLUDE_DIRS} )

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