include_directories(${OpenCV_INCLUDE_DIRS})
add_executable(run_vo-0.2 run_vo.cpp)
target_link_libraries(run_vo-0.2 myslam-0.2)