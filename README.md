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
На основе статьи https://habr.com/ru/articles/414109/

Сборка и запуск
Для сборки нашего приложения и создания Docker-образа достаточно будет выполнить следующую команду:

# Здесь docker-cpp-sample название нашего образа
# . - подразумевает путь к директории, содержащей Dockerfile
docker build -t docker-cpp-sample .
# Для запуска приложения используем команду:
docker run docker-cpp-sample
# Для передачи параметра достаточно будет добавить его в вышеприведенную команду:
docker run docker-cpp-sample --help
Allowed options:
  -h [ --help ]         Produce this message
