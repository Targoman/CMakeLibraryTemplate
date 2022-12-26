cmake_minimum_required(VERSION 3.16)
project(CMakeBuildSampleLib VERSION 0.0.1)

include(./Targoman.cmake)
setup_bs_paths()

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

option(COMPILE_OPTIONAL_TEST "Compile optional blackbox test set" FALSE)
option(COMPILE_EXAMPLES "Compile examples" FALSE)

find_package(Qt5 COMPONENTS Core Test REQUIRED)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

add_library(SampleLibrary
    SHARED
    libsrc/libSampleLibrary/clsSample.cpp
)
set_target_properties(SampleLibrary
    PROPERTIES
    PUBLIC_HEADER
    libsrc/libSampleLibrary/clsSample.h
)
target_link_libraries(SampleLibrary Qt5::Core)

export_public_headers(SampleLibrary)

add_subdirectory(unitTests)
add_subdirectory(tests)
add_subdirectory(apps)
add_subdirectory(examples)