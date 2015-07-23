helloworld project using CMake
==============================

Instructions:
```
mkdir -p cmake-tests/test-lib
cd cmake-tests/test-lib
git clone https://github.com/winksaville/cmake-tests-test-lib .
mkdir build
cd build
cmake ..
make
app/test-lib
```

This is an example of using libraries with CMake. It builds both static and shared
libraries and the app can choose which to use. Its main claim is that it is an
example of creating a library and how to use target_link_libraries to use a library
and target_compile_definitions and target_include_directories to provide -D and -I
compiler flags when using them.

Using [cmake-buildsystem(7)](http://www.cmake.org/cmake/help/v3.3/manual/cmake-buildsystem.7.html)
provides a good explanation of how to structure a CMake build system.
