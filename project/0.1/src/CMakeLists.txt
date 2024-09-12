add_library(myslam-1.0 SHARED
        frame.cpp
        mappoint.cpp
        map.cpp
        camera.cpp
        config.cpp
)

target_link_libraries(myslam-1.0
        ${THIRD_PARTY_LIBS}
)
