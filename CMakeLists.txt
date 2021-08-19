# Minimum version of CMake required to build this project
cmake_minimum_required(VERSION 3.0)

# Name of the project
project(Project)

# For conan
include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

# Create new variables for folder names
set(HELPERS_DIR src/helpers)
set(MODELS_DIR src/models)

# Add all the source files needed to build the executable
add_executable(
    Project 
    src/main.cpp 
    ${HELPERS_DIR}/AwesomeHelper.cpp 
    ${HELPERS_DIR}/OkHelper.cpp 
    ${MODELS_DIR}/Person.cpp
)

# Include the directory where MyLibrary project is
# library
add_subdirectory(libraries/MyLibrary)

# Link the executable and the library together
target_link_libraries(Project MyLibrary ${CONAN_LIBS})