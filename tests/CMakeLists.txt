cmake_minimum_required(VERSION 3.16)

add_executable(${CMAKE_PROJECT_NAME}_test1 test1/main.cpp)
target_link_libraries(${CMAKE_PROJECT_NAME}_test1 SampleLibrary)
target_link_libraries(${CMAKE_PROJECT_NAME}_test1 Qt5::Core)
add_executable(${CMAKE_PROJECT_NAME}_test2 test2/main.cpp)
target_link_libraries(${CMAKE_PROJECT_NAME}_test2 SampleLibrary)
target_link_libraries(${CMAKE_PROJECT_NAME}_test2 Qt5::Core)

if(COMPILE_OPTIONAL_TEST)
    add_executable(${CMAKE_PROJECT_NAME}_test3 optionalTest/main.cpp)
    target_link_libraries(${CMAKE_PROJECT_NAME}_test3 SampleLibrary)
    target_link_libraries(${CMAKE_PROJECT_NAME}_test3 Qt5::Core)
endif()