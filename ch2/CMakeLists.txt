# 添加一个可执行程序
# 语法：add_executable( 程序名 源代码文件 ）
add_executable(helloSLAM helloSLAM.cpp)
# 共享库
add_library(hello_shared SHARED libHelloSLAM.cpp)

add_executable(useHello useHello.cpp)
# 将库文件链接到可执行程序上
target_link_libraries(useHello hello_shared)
