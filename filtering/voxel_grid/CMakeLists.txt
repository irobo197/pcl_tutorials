cmake_minimum_required(VERSION 2.8.3)
 
project(voxel_grid)
 
find_package(PCL REQUIRED)
 
include_directories(
  ${PCL_INCLUDE_DIRS}
)

link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (voxel_grid
  src/voxel_grid.cpp
)
target_link_libraries (voxel_grid
  ${PCL_LIBRARIES}
)
