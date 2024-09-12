add_executable(eigenMatrix useEigen/eigenMatrix.cpp)

add_executable(eigenGeometry useGeometry/eigenGeometry.cpp)

add_executable(visualizeGeometry visualizeGeometry/visualizeGeometry.cpp)
target_link_libraries(visualizeGeometry ${Pangolin_LIBRARIES})