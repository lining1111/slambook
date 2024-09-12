set(THIRD_PARTY_LIBS
        ${OpenCV_LIBS}
        ${Sophus_LIBRARIES}
)

add_executable(dense_mapping dense_monocular/dense_mapping.cpp)
target_link_libraries(dense_mapping ${THIRD_PARTY_LIBS})


add_executable(pointcloud_mapping dense_RGBD/pointcloud_mapping.cpp)
target_link_libraries(pointcloud_mapping ${OpenCV_LIBS} ${PCL_LIBRARIES})

add_executable(octomap_mapping dense_RGBD/octomap_mapping.cpp)
target_link_libraries(octomap_mapping ${OpenCV_LIBS} ${PCL_LIBRARIES} ${OCTOMAP_LIBRARIES})