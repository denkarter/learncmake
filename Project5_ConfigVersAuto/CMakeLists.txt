# 0.) Create source and cmake file
# 1.) mkdir build
# 2.) cd build
# 3.) cmake ..     - Generating Build files / Configure the project
# 4.) cmake --build .
# 5.) ./Executable

cmake_minimum_required(VERSION 3.22)

project(
    ProjectLearnCmake
    VERSION 1.0.0
    LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

set(LIBRARY_NAME Library)
set(EXECUTABLE_NAME Executable)

option(COMPILE_EXECUTABLE "Whether to compile executable" ON)
# Example to use in terminal:
# cmake .. -DCOMPILE_EXECUTABLE=ON

add_subdirectory(configured)
add_subdirectory(src)   # adding directory of Library
if(COMPILE_EXECUTABLE)
    add_subdirectory(app)   # adding directory of Executable
else()
    message("W/o exe compiling")
endif()
