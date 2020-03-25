cmake_minimum_required(VERSION 3.1)

project(cluster_extraction)

find_package(PCL REQUIRED)
find_package(CUDA)
include(FindCUDA)

include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (cluster_extraction cluster_extraction.cpp)
target_link_libraries (cluster_extraction ${PCL_LIBRARIES})