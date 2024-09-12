add_executable(feature_training feature_training.cpp)
target_link_libraries(feature_training ${OpenCV_LIBS} ${DBoW3_LIBS})

add_executable(loop_closure loop_closure.cpp)
target_link_libraries(loop_closure ${OpenCV_LIBS} ${DBoW3_LIBS})

add_executable(gen_vocab gen_vocab_large.cpp)
target_link_libraries(gen_vocab ${OpenCV_LIBS} ${DBoW3_LIBS})