cmake_minimum_required(VERSION 3.20)
project(DracoEngine LANGUAGES CXX C)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(external/glfw)

add_executable(draco_engine
    src/main.cpp
    external/glad/src/glad.c
)

target_include_directories(draco_engine PUBLIC external/glad/include)
target_link_libraries(draco_engine glfw opengl32)