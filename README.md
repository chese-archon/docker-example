Сборка C++ проекта при помощи Docker.

В качестве проекта будем подразумевать CommandLine приложение, выводящее строку "Hello World!" в стандартный поток вывода.

В проекте будет использован необходимый минимум библиотек, а также CMake в качестве системы сборки.
Структура проекта:

project
|   Dockerfile
|
\---src
        CMakeLists.txt
        main.cpp
        sample_hello_world.h
        test.cpp
