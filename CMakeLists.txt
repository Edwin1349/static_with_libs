# CMakeList.txt : CMake project for test, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)
project(test)
# Add source to this project's executable.

add_subdirectory(libs/shared)
add_subdirectory(libs/shared_static)

add_executable(${PROJECT_NAME}
    main.cpp
)

target_link_libraries(${PROJECT_NAME} MyLib_static)
target_link_libraries(${PROJECT_NAME} MyLib)
target_link_libraries(${PROJECT_NAME} MyLib_shared_static)

# TODO: Add tests and install targets if needed.
