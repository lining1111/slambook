# 添加头文件
include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(imageBasics imageBasics/imageBasics.cpp)
# 链接OpenCV库
target_link_libraries(imageBasics ${OpenCV_LIBS})

add_executable(joinMap joinMap/joinMap.cpp)
target_link_libraries(joinMap ${OpenCV_LIBS} ${PCL_LIBRARIES})