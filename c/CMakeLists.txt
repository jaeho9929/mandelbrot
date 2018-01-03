project(mandelbrot C)
cmake_minimum_required(VERSION 3.0)

find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
include_directories(${OPENGL_INCLUDE_DIRS} ${GLUT_INCLUDE_DIRS})

add_executable(${PROJECT_NAME}.out mandelbrot.c)
target_link_libraries(${PROJECT_NAME}.out ${OPENGL_LIBRARIES} ${GLUT_LIBRARY} m)
