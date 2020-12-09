cmake_minimum_required(VERSION 3.0.0)
project(ucGui VERSION 0.1.0)

include(CTest)
enable_testing()

include_directories(
    ${CMAKE_CURRENT_SOURCE_DIR}/GUI/Core 
    ${CMAKE_CURRENT_SOURCE_DIR}/Config
    ${CMAKE_CURRENT_SOURCE_DIR}/GUI/WM
    ${CMAKE_CURRENT_SOURCE_DIR}/GUI/Widget
                    )

file(GLOB_RECURSE   DIR_SRCS  *.c)
MESSAGE(STATUS  ${PROJECT_SOURCE_DIR})

#
add_library(ucGui SHARED  ${DIR_SRCS})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

target_link_libraries( ${PROJECT_NAME} m)