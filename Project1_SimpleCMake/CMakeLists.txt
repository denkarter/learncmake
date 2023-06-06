# 0.) Create source and cmake file
# 1.) mkdir build
# 2.) cd build
# 3.) cmake ..     - Generating Build files / Configure the project
# 4.) cmake --build .
# 5.) ./Executable

cmake_minimum_required(VERSION 3.22)
project(
    Project1SimpleCMake
    VERSION 1.0.0
    LANGUAGES C CXX)
add_executable(Executable main.cc)
