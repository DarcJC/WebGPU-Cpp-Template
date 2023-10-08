cmake_minimum_required(VERSION 3.12)

project(WebGPUTemplate)

add_executable(MyApp Source/main.cpp)
set_property(TARGET MyApp PROPERTY CXX_STANDARD 23)

find_package(WebGPU PATHS ThirdParty/WebGPU-Cpp/CMake NO_DEFAULT_PATH REQUIRED)
target_link_libraries(MyApp PUBLIC WebGPU)
target_copy_webgpu_binaries(MyApp)

find_package(glfw3 CONFIG REQUIRED)
target_link_libraries(MyApp PRIVATE glfw)

add_subdirectory(ThirdParty/GLFWWebGPU)
target_link_libraries(MyApp PRIVATE glfw3webgpu)
