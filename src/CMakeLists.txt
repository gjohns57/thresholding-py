cmake_minimum_required(VERSION 3.9)
project(thresholdinglib VERSION 1.0.1 DESCRIPTION "C++ library for python thresholding package.")
add_library(thresholdinglib SHARED cpp-src/test.c)
find_package(PythonLibs REQUIRED)
include_directories(${PYTHON_INCLUDE_DIRS})
target_link_libraries(thresholdinglib ${PYTHON_LIBRARIES})