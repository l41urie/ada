cmake_minimum_required(VERSION 3.19)

project(ada)

add_subdirectory(contrib)

set(ADA_COMPILE_OPTIONS
    -std=c++23
)

add_subdirectory(win_agent)

target_include_directories(win_agent PRIVATE shared)

add_subdirectory(test_program)
