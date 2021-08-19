# C++ project template with CMake and Conan

cmake: https://ncona.com/2019/03/building-a-cpp-project-with-cmake/

conan: https://docs.conan.io/en/latest/getting_started.html

### Package manager - conan

conanfile.txt - specify the requried packages and generator (cmake in this case)

### Buildsystem - make

### Buildsystem generator - CMake

CMakeLists.txt - specify the project libraries and dependencies. Add conan libs.

### Commands to run

1. cd build
2. conan install ..
3. cmake ..
4. make
5. ./bin/Project

---

## Nested CMake file for MyLibrary

The project has a nested CMake for the library files. It defines a project and adds itself as a library to the project. 

There is no "add_executable" section in CMake since we do not need an executbale here and there is no main() defined for the MyProject.cpp anyway.

So, this will just compile the library and generate an object file (*.o) without linking it to anything. Equivalent to 

`g++ -c MyLibrary.cpp`

To link a libray to the main project, if not using CMake, run:

`g++ ../libraries/MyLibrary/src/MyLibrary.cpp main.cpp -o main`

---

## C++ Build Process

source code -> (**Preprocessor**) -> exp. temp file 

temp file -> (**Compiler**) -> assembler code 

assembler code -> (**Assembler**) -> machine code (.o/.obj)

machine code -> (**Linker**) -> executbale (.exe)