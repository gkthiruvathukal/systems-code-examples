project("pthreads")

cmake_minimum_required(VERSION 2.6)

# https://stackoverflow.com/questions/6594796/how-do-i-make-cmake-output-into-a-bin-dir
# We only need 'bin' here.

if (CMAKE_VERSION VERSION_LESS "3.1")
  add_definitions(-std=c++11)
else()
  set(CMAKE_CXX_STANDARD 11)
  set(CMAKE_CXX_STANDARD_REQUIRED ON)
  set(CMAKE_CXX_EXTENSIONS OFF)
endif()

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
add_executable(strbuffer_demo strbuffer_demo.c strbuffer.c)

add_executable(strbuffer_getline_demo strbuffer_getline_demo.c strbuffer.c)
