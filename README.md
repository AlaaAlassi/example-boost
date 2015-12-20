# example-boost
Project to reuse the Boost package created with Conan C and C++ package manager

Instructions:

```bash
$ git clone https://github.com/memsharded/example-boost.git
$ cd example-boost
$ mkdir build && cd build
$ conan install ..
$ cmake .. -G "Visual Studio 14 Win64"
$ cmake --build . --config Release
$ cd bin
$ regex
```