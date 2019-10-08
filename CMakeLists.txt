
cmake_minimum_required(VERSION 3.1)
project(glred)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

find_package(OpenGL REQUIRED)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/glfw)

add_executable(${PROJECT_NAME} glred.cpp)
target_link_libraries(${PROJECT_NAME} glfw ${OPENGL_gl_LIBRARY})
