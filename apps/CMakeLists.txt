cmake_minimum_required(VERSION 3.16)

add_executable(sampleApp sampleApp/main.cpp)
target_link_libraries(sampleApp SampleLibrary)
target_link_libraries(sampleApp Qt5::Core)