cmake_minimum_required(VERSION 3.9)
project(wiringPi)

set(CMAKE_CXX_STANDARD 11)

file(GLOB SOURCES
        "wiringPi/*.h"
        "wiringPi/*.c"
)

include_directories(wiringPi)

add_library(wiringPi ${SOURCES})
target_link_libraries(wiringPi pthread rt)