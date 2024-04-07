# CMake 简单使用
## 目录结构


## 内置函数

生成可执行文件

```add_executable(main main.cpp)```

## 内置宏

设置编译类型

```CMAKE_BUILD_TYPE "Release"```

## 执行
```cpp
    mkdir build
    cd build
    cmake ..
    make
    ./main

    // 输出：
    hello world!
```