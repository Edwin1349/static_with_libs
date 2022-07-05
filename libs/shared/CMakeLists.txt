# CMakeList.txt : CMake project for test, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)
# Add source to this project's executable.

set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS TRUE)

add_library(MyLib SHARED "../src/test.cpp")
add_library(MyLib_static STATIC "../src/test.cpp")

#target_link_libraries(shared_static_lib static_lib)
# TODO: Add tests and install targets if needed.
