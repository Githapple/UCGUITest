cmake_minimum_required(VERSION 3.0.0)
project(ucGui VERSION 0.1.0)

include(CTest)
enable_testing()

file(GLOB_RECURSE ./GUI *.c)
# file(GLOB_RECURSE HDRS *.h)

MESSAGE( STATUS "this var key = ${GLOB_RECURSE}")
add_library(ucGui ucGui.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
