add_library( myslam-3.0 SHARED
    frame.cpp
    mappoint.cpp
    map.cpp
    camera.cpp
    config.cpp
    g2o_types.cpp
    visual_odometry.cpp
)

target_link_libraries( myslam-3.0
    ${THIRD_PARTY_LIBS}
)