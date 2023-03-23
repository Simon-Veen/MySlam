cmake_minimum_required(VERSION 2.8)
set(CMAKE_BUILD_TYPE "Debug")
project(HelloSlam)

add_executable(hellowolrd helloworld.cpp)
add_executable(useHello useHello.cpp)
add_library(hello_shared SHARED libhelloworld.cpp)

target_link_libraries(useHello hello_shared)

