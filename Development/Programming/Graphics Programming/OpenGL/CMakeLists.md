If you are done with [[Prerequisites]] prepration, you can continue with following cmake setup steps:
- Create your project folder
- Create subfolder where it contains **/glad** and **/sdl**
- Create **/src** subfolder where your source code locates to
- Create **/include** subfolder
- Create a **CMakelists.txt** inside **/glad** folder:
```
cmake_minimum_require(VERSION 3.16)

project(glad)

add_library(glad STATIC src/glad.c)

add_library(glad::glad ALIAS glad)

target_include_directories(glad PUBLIC include)
```
- Create **CMakelists.txt** in your main directory:\
```
cmake_minimum_require(VERSION 3.16)

project(MyOpenGL)

add_executable(${PROJECT_NAME} src/main.cpp)

add_subdirectory(vendor/sdl)
add_subdirectory(vendor/glad)

target_link_libraries(${PROJECT_NAME} PRIVATE SDL3::SDL3 glad::glad)
```
- Start the build by vscode extension or using following commands:
```
mkdir build
cd build
cmake ..
```
- After done building run command `make` in build folder to generate binary file (.exe)