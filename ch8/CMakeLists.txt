set(G2O_LIBS
        g2o_core g2o_types_sba g2o_solver_csparse g2o_stuff g2o_csparse_extension
)

add_executable(direct_sparse directMethod/direct_sparse.cpp)
target_link_libraries(direct_sparse ${OpenCV_LIBS} ${G2O_LIBS})

add_executable(direct_semidense directMethod/direct_semidense.cpp)
target_link_libraries(direct_semidense ${OpenCV_LIBS} ${G2O_LIBS})


add_executable(useLK LKFlow/useLK.cpp)
target_link_libraries(useLK ${OpenCV_LIBS})