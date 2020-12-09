cmake_minimum_required(VERSION 3.0.0)

project(ucGuiTest VERSION 0.1.0)
include_directories(
    ${CMAKE_CURRENT_SOURCE_DIR}/GUI/Core 
    ${CMAKE_CURRENT_SOURCE_DIR}/Config
    ${CMAKE_CURRENT_SOURCE_DIR}/GUI/WM
    ${CMAKE_CURRENT_SOURCE_DIR}/GUI/Widget
                    )

file(GLOB_RECURSE   DIR_SRCS  Application/*.c)

# link_directories(${PROJECT_SOURCE_DIR}/build/GUI/)

MESSAGE(STATUS "this path is = ${PROJECT_SOURCE_DIR} " )
MESSAGE(STATUS "tDIR_SRCS is = ${DIR_SRCS} " )
add_subdirectory(GUI)
# link_directories()

add_executable(ucGuiTest ${DIR_SRCS} )

target_link_libraries(${PROJECT_NAME}  ucGui)
