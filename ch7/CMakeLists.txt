add_executable(feature_extraction feature_extraction.cpp)
target_link_libraries(feature_extraction ${OpenCV_LIBS})

# add_executable( pose_estimation_2d2d pose_estimation_2d2d.cpp extra.cpp ) # use this if in OpenCV2 
add_executable(pose_estimation_2d2d pose_estimation_2d2d.cpp)
target_link_libraries(pose_estimation_2d2d ${OpenCV_LIBS})

# add_executable( triangulation triangulation.cpp extra.cpp) # use this if in opencv2 
add_executable(triangulation triangulation.cpp)
target_link_libraries(triangulation ${OpenCV_LIBS})

set(G2O_LIBS g2o_core g2o_stuff g2o_types_sba g2o_csparse_extension g2o_solver_csparse g2o_types_slam3d)

add_executable(pose_estimation_3d2d pose_estimation_3d2d.cpp)
target_link_libraries(pose_estimation_3d2d
        ${OpenCV_LIBS}
        ${G2O_LIBS}
)

add_executable(pose_estimation_3d3d pose_estimation_3d3d.cpp)
target_link_libraries(pose_estimation_3d3d
        ${OpenCV_LIBS} glog
        ${G2O_LIBS}
)
