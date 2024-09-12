add_library( myslam-2.0 SHARED
    frame.cpp
    mappoint.cpp
    map.cpp
    camera.cpp
    config.cpp
    visual_odometry.cpp
)

target_link_libraries( myslam-2.0
    ${THIRD_PARTY_LIBS}
)
