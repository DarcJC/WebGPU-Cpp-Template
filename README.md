# WebGPU Template Project

## Requirements

1. Install [vcpkg](https://github.com/microsoft/vcpkg/blob/master/README.md) [中文](https://github.com/microsoft/vcpkg/blob/master/README_zh_CN.md)
2. Generating cmake files with flag `-DCMAKE_TOOLCHAIN_FILE=/PATH/TO/vcpkg/scripts/buildsystems/vcpkg.cmake`
3. Install required packages

```bash
vcpkg install glfw3:x64-windows
```

## Build

```bash
cmake -DCMAKE_BUILD_TYPE=Debug -DCMAKE_TOOLCHAIN_FILE=/PATH/TO/YOUR/VCPKG/CMAKE -B build
cmake --build build --target MyApp
```

## Reference

Code is copied from [LearnWebGPU](https://github.com/eliemichel/LearnWebGPU-Code/tree/step030).
