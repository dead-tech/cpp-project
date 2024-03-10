cmake_minimum_required(VERSION 3.10)

set(PROJECT_NAME "cpp-project")
project(${PROJECT_NAME} VERSION 0.0.1 DESCRIPTION "" LANGUAGES CXX C)

set(COMPILER_WARNINGS
    "-Wall"
    "-Wextra"
    "-Werror"
    "-Wconversion"
    "-Wpedantic"
    "-Wshadow"
    "-Wnon-virtual-dtor"
    "-Wold-style-cast"
    "-Wcast-align"
    "-Wunused"
    "-Woverloaded-virtual"
    "-Wnull-dereference"
    "-Wdouble-promotion"
    "-Wimplicit-fallthrough"
    "-Wmisleading-indentation"
    "-Wduplicated-branches"
    "-Wduplicated-cond"
    "-Wlogical-op"
    "-Wuseless-cast"
    "-fsantize=undefined,address"
)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_FLAGS ${COMPILER_WARNINGS})

set(SOURCES
    "${CMAKE_SOURCE_DIR}/src/main.cpp"
)

add_executable(${PROJECT_NAME} ${SOURCES})
