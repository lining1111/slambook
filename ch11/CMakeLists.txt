add_executable(pose_graph_g2o_SE3 pose_graph_g2o_SE3.cpp)
target_link_libraries(pose_graph_g2o_SE3
        g2o_core g2o_stuff g2o_types_slam3d g2o_solver_cholmod
)

add_executable(pose_graph_g2o_lie pose_graph_g2o_lie_algebra.cpp)
target_link_libraries(pose_graph_g2o_lie
        glog
        g2o_core g2o_stuff
        g2o_solver_cholmod
        ${Sophus_LIBRARIES}
)

add_executable(pose_graph_gtsam pose_graph_gtsam.cpp)
target_link_libraries(pose_graph_gtsam
        g2o_solver_cholmod gtsam
)
