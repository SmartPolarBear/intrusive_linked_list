cmake_minimum_required(VERSION 3.16)

add_executable(ds_main main.cpp ../include/utility.h)

target_include_directories(ds_main PRIVATE include)