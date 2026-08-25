cmake_minimum_required(VERSION 3.16)

project(inih LANGUAGES C CXX)

add_library(inih STATIC
    ini.c
    cpp/INIReader.cpp
)

target_include_directories(inih PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_CURRENT_SOURCE_DIR}/cpp
)

target_compile_features(inih PUBLIC cxx_std_11)

add_library(inih::inih ALIAS inih)