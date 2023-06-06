# 0.) Create source and cmake file
# 1.) mkdir build
# 2.) cd build
# 3.) cmake ..     - Generating Build files / Configure the project
# 4.) cmake --build .
# 5.) ./Executable

cmake_minimum_required(VERSION 3.22)

project(
    Prj2FoldersInCmake
    VERSION 1.0.0
    LANGUAGES C CXX)

add_library(Library STATIC my_lib.cc)   # It's a second target...
add_executable(Executable main.cc)
target_link_libraries(Executable PUBLIC Library)   # We link library to our first target - Executable

# cmake --build . --target Library // only Library will build
