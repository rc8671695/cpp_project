# Minimum version of CMake required to build this project
cmake_minimum_required(VERSION 3.0)

# Name of the project
project(MyLibrary)

# Add a library to this build
add_library(MyLibrary src/MyLibrary.cpp)