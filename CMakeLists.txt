cmake_minimum_required(VERSION 3.17)

project(fractals VERSION 0.1.0)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_CURRENT_SOURCE_DIR}/cmake/modules)
set(PLATFORM ${CMAKE_CURRENT_SOURCE_DIR}/cmake/platform)
set(EXTERNAL ${CMAKE_CURRENT_SOURCE_DIR}/third_party)
set(FRACTALS ${CMAKE_CURRENT_SOURCE_DIR})

if (APPLE)
    include(${PLATFORM}/apple.cmake)
endif()

add_subdirectory(${EXTERNAL}/glad)
add_subdirectory(${EXTERNAL}/glfw)
add_subdirectory(${FRACTALS}/src)
