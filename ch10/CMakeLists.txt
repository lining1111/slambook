add_library(ceresBALProblem SHARED ceres_custombundle/common/BALProblem.cpp)
add_library(ceresParseCmd SHARED ceres_custombundle/common/flags/command_args.cpp)

add_executable(ceres_customBundle ceres_custombundle/ceresBundle.cpp)

target_link_libraries(ceres_customBundle ceresBALProblem ceresParseCmd ${CERES_LIBRARIES} )


SET(G2O_LIBS g2o_cli g2o_ext_freeglut_minimal g2o_simulator g2o_solver_slam2d_linear
        g2o_types_icp g2o_types_slam2d g2o_types_sba g2o_types_slam3d g2o_core g2o_interface
        g2o_solver_csparse g2o_solver_structure_only g2o_csparse_extension g2o_opengl_helper g2o_solver_dense
        g2o_stuff g2o_types_sclam2d g2o_parser g2o_solver_pcg g2o_types_data g2o_types_sim3 cxsparse )


add_library(g2oBALProblem SHARED g2o_custombundle/common/BALProblem.cpp)
add_library(g2oParseCmd SHARED g2o_custombundle/common/flags/command_args.cpp)

add_executable(g2o_customBundle g2o_custombundle/g2o_bundle.cpp)

target_link_libraries(g2o_customBundle ${G2O_LIBS} ${CHOLMOD_LIBRARIES} g2oBALProblem g2oParseCmd)