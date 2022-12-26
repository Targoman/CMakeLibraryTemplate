cmake_minimum_required(VERSION 3.16)

add_executable(example1 ./main.cpp)
target_link_libraries(example1 SampleLibrary)
target_link_libraries(example1 Qt5::Core)