cmake_minimum_required(VERSION 3.10)
project(main VERSION 0.1.0)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_compile_options(
    "$<$<CONFIG:DEBUG>:-fsanitize=address,undefined>"
    "-Wall"
    "-Wextra"
)
add_link_options("$<$<CONFIG:DEBUG>:-fsanitize=address,undefined>")

add_executable(main main.cpp)
