cmake_minimum_required(VERSION 3.0)
project(hde C)

add_library(hde OBJECT
    include/hde32.h
    include/hde64.h
    src/hde32.c
    src/hde64.c
    src/table32.h
    src/table64.h)
    
add_executable(hde_example examples/example.c)
target_link_libraries(hde_example hde)