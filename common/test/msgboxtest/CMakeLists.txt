cmake_minimum_required(VERSION 2.6)
set(CMAKE_VERBOSE_MAKEFILE ON)
project(mbtest)
add_definitions("-Wall -g")
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
# add dependency
include_directories(/usr/local/include ../../../efnfw ../../include ../../src)
link_directories(/usr/local/lib ../../../efnfw/lib ../../lib)
link_libraries(libcommon.a libefnfw.a protobuf hiredis json)
set(SRC_LISTS msgboxtest.cpp)
add_executable(mbtest ${SRC_LISTS})
