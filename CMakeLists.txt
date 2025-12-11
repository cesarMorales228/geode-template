cmake_minimum_required(VERSION 3.13)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(MyCustomMod)

# Si la acción de Geode exporta GEODE_SDK, añadimos el módulo
if(DEFINED ENV{GEODE_SDK})
    list(APPEND CMAKE_MODULE_PATH "$ENV{GEODE_SDK}/share/cmake/Geode")
endif()

find_package(Geode REQUIRED)

setup_geode_mod(MyCustomMod)

add_geode_sources(MyCustomMod
    src/main.cpp
)
