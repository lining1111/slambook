add_library(myslam-0.2 SHARED
        frame.cpp
        mappoint.cpp
        map.cpp
        camera.cpp
        config.cpp
        visual_odometry.cpp
)

target_link_libraries(myslam-0.2
        ${THIRD_PARTY_LIBS}
)
