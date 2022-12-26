cmake_minimum_required(VERSION 3.16)

add_executable(${CMAKE_PROJECT_NAME}_unitTest ./UnitTest.cpp)
target_link_libraries(${CMAKE_PROJECT_NAME}_unitTest Qt5::Core Qt5::Test)
target_link_libraries(${CMAKE_PROJECT_NAME}_unitTest SampleLibrary)
