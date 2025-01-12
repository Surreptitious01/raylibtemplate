cmake_minimum_required(VERSION 3.10)

project(raylibtemplate)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED YES)

# Add raylib as a subdirectory
add_subdirectory(external/raylib)

# Add your source files
add_executable(raylibtemplate src/main.c)

# Link raylib to your project
target_link_libraries(raylibtemplate raylib)

# If raylib is built locally, you might need to link OpenGL manually
find_package(OpenGL REQUIRED)
target_link_libraries(raylibtemplate OpenGL::GL)
