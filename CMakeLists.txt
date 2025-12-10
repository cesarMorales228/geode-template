cmake_minimum_required(VERSION 3.13)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(MyCustomMod)

# Geode ya debería ser encontrado porque le pasamos la ruta en el comando de build
find_package(Geode REQUIRED)

setup_geode_mod(MyCustomMod)

add_geode_sources(MyCustomMod
    src/main.cpp
)
