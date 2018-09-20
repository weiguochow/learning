CMakeLists.txt to compiple opencv and pcl


cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

project(cloud_viewer)

find_package(OpenCV REQUIRED)
find_package(PCL 1.2 REQUIRED)

include_directories(${OpenCV_INCLUDE_DIRS})
include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (cloud_viewer cloud_viewer.cpp kernel.cu)

target_link_libraries(cloud_viewer ${OpenCV_LIBS})
target_link_libraries (cloud_viewer ${PCL_LIBRARIES})



Note:
OpenCV_DIRS = the directory contains OpenCVConfig.cmake
