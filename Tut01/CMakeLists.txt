cmake_minimum_required(VERSION 3.0.0)

project(DeepPurple VERSION 0.1 LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTOMOC ON)


include_directories(
        /usr/include/
        )
find_package(OpenGL REQUIRED)

set(ALL_LIBS
        ${OPENGL_LIBRARY}
        glfw
        GLEW
)

add_executable(${PROJECT_NAME} "main.cpp")

target_link_libraries(DeepPurple
        ${ALL_LIBS}
)
