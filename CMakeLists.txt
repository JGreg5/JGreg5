cmake_minimum_required(VERSION 3.22.1)

project(Hello VERSION 0.0.1)


include(env.cmake)
set(CMAKE_C_COMPILER TOOLCHAIN_PATH)

#create a sources variable with a link to all *.c files to compile
set(SOURCES
    src/hello.c
    src/main.c)

add_executable(helloworld ${SOURCES})

target_include_directories(helloworld
    PUBLIC
        ${PROJECT_SOURCE_DIR}/include)

message(STATUS "CMAKE SOURCE DIR = ${CMAKE_SOURCE_DIR}")
message(STATUS "CMAKE CURRENT SOURCE DIR = ${CMAKE_CURRENT_SOURCE_DIR}")
message(STATUS "PROJECT SOURCE DIR = ${PROJECT_SOURCE_DIR}")
message(STATUS "CMAKE BINARY DIR = ${CMAKE_BINARY_DIR} ")
message(STATUS "CMAKE CURRENT BINARY DIR = ${CMAKE_CURRENT_BINARY_DIR}")
message(STATUS "PROJECT BINARY DIR = ${PROJECT_BINARY_DIR}")
message(STATUS "CMAKE TOOL PATH = ${CMAKE_TOOLCHAIN_FILE}")
message(STATUS "TOOLCHAIN PATH = ${TOOLCHAIN_PATH}")