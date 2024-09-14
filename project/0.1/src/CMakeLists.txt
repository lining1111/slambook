add_library(myslam-0.1 SHARED
        frame.cpp
        mappoint.cpp
        map.cpp
        camera.cpp
        config.cpp
)

target_link_libraries(myslam-0.1
        ${THIRD_PARTY_LIBS}
)
