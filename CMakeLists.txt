cmake_minimum_required (VERSION 3.15)

project(example)

add_subdirectory(static-lib)

set(SOURCE_FILES main.cpp)

add_executable (example ${SOURCE_FILES})

# Connecting the library, specify where to get the header files
include_directories(static-lib)
# And also we specify dependence on static library
target_link_libraries(example ${CMAKE_SOURCE_DIR}/cmake-build-debug/static-lib/libstatic_lib.a)