set(THIRD_PARTY_LIBS
        ${OpenCV_LIBS}
        ${Sophus_LIBRARIES}
        g2o_core g2o_stuff g2o_types_sba
)
############### dependencies ######################
include_directories(include)
add_subdirectory(src)
add_subdirectory(test)