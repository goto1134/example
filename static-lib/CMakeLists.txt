cmake_minimum_required (VERSION 3.8)

project(static_lib)

set(SOURCE_FILES static_lib.cpp)
set(HEADER_FILES static_lib.h)

add_library(static_lib STATIC ${HEADER_FILES} ${SOURCE_FILES})