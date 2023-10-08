# WebGPU Template Project

## Requirements

1. Install [vcpkg](https://github.com/microsoft/vcpkg/blob/master/README.md) [安装vcpkg](https://github.com/microsoft/vcpkg/blob/master/README_zh_CN.md)

2. Generating cmake files with flag 
   添加vcpkg为CMake工具链文件

```bash
-DCMAKE_TOOLCHAIN_FILE=/PATH/TO/vcpkg/scripts/buildsystems/vcpkg.cmake
```

3. Install required packages 
   安装所需依赖

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
