cmake_minimum_required(VERSION 2.6)

PROJECT(raycast)

set (CMAKE_CXX_COMPILER F:/Programming/MinGW/bin/gcc.exe)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -g -Wall -Wextra -finline-functions")
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin)

include_directories($(raycast_SOURCE_DIR)/include)
add_subdirectory(src)