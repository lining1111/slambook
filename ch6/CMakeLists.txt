add_executable(ceres_curve_fitting ceres_curve_fitting/main.cpp)
# 与Ceres和OpenCV链接
target_link_libraries(ceres_curve_fitting ${CERES_LIBRARIES} ${OpenCV_LIBS})

add_executable(g2o_curve_fitting g2o_curve_fitting/main.cpp)
# 与G2O和OpenCV链接
target_link_libraries(g2o_curve_fitting
        ${OpenCV_LIBS}
        g2o_core g2o_stuff)