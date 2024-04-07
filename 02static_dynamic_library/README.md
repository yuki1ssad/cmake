# 2 生成与使用库文件

使用add_library命令可以生成：

静态库

动态库

对象库

...

## 目录结构

```
02static_dynamic_library/
├── CMakeLists.txt
├── README.md
├── hello
│   ├── CMakeLists.txt
│   ├── hello.cpp
│   └── hello.h
├── main
│   ├── CMakeLists.txt
│   └── main.cpp
└── world
    ├── CMakeLists.txt
    ├── world.cpp
    └── world.h
```

## 静态库

* STATIC 必须要大写

```add_library(world STATIC world.h world.cpp)```

## 动态库

* SHARED 必须要大写

```add_library(world SHARED world.h world.cpp)```

## 依赖关系

* 为了保证在执行main之前，先执行hello和world。

```add_dependencies(main hello world)```

## 执行
```cpp
    mkdir build
    cd build
    cmake ..
    make
    ./main/main

    // 输出：
    hello
     world!
```

