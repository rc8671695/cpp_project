# C++ Project template with CMake and Conan

cmake: https://ncona.com/2019/03/building-a-cpp-project-with-cmake/

conan: https://docs.conan.io/en/latest/getting_started.html

### Package manager - conan

conanfile.txt - specify the requried packages and generator (cmake in this case)

### Buildsystem - make

### Buildsystem generator - CMake

CMakeLists.txt - speify the project libraries and dependencies. Add conan libs.

### Commands to run

1. cd build
2. conan install ..
3. cmake ..
4. make
5. ./bin/Project