cmake_minimum_required(VERSION 3.24.2)

project(CLASS_STRING LANGUAGES CXX)

set(SOURCE_LIB String.cpp String.hpp StringException.hpp)

set(SOURCE_EXE main.cpp)

add_library(str_lib ${SOURCE_LIB})

add_executable(src_str ${SOURCE_EXE})

target_link_libraries(src_str str_lib)

set_target_properties(
    src_str PROPERTIES 
    CMAKE_CXX_STANDARD 11
    CXX_STANDARD_REQUIRED ON
)