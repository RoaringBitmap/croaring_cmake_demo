# Simple demo of CRoaring as a CMake dependency.

This repository is meant to serve as an example of how to use [CRoaring](https://github.com/RoaringBitmap/CRoaring) as a `CMake` dependency by having CRoaring as a git submodule. 

Usage:

```
mkdir build && cd build && cmake .. && cmake --build . && ./src/test
```

The simple `CMake` project builds a simple test (`./src/test`) .

Please refer to the main [CRoaring](https://github.com/RoaringBitmap/CRoaring) project for further documentation.

## How to add simdjson as a CMake dependency

Fundamentally, it is as simple as adding the following line after copying the project as a subdirectory in your own project:

```
add_subdirectory(CRoaring EXCLUDE_FROM_ALL)
```

## Why and how to add a submodule?

If your own project is under git, you probably do not want to copy CRoaring in your own git repository. Instead, you want to add it as a submodule.


Once you have a git repository, adding simdjson as a submodule is relatively easy, type:

```
git submodule add https://github.com/RoaringBitmap/CRoaring.git
```

Using submodules, you can control exactly which version your colleagues are using, down to the commit. Furthermore, submodules are portable: they work wherever git works.


Then you can just follow our example.

