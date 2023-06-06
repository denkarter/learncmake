add_library(Library STATIC my_lib.cc)
target_include_directories(Library PUBLIC "./")   # where we can find header file, "./" - in the same directory
