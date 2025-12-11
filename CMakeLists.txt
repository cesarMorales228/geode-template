cmake_minimum_required(VERSION 3.13)

project(MyCustomMod)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# IMPORTANTE: no tocar GEODE_SDK ni find_package aquí

# Esta macro la provee el template de Geode incluido en el repo
setup_geode_mod(MyCustomMod)

add_geode_sources(MyCustomMod
    src/main.cpp
)
