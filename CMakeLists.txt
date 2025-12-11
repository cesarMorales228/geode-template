cmake_minimum_required(VERSION 3.13)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(MyCustomMod)

# 1) AÑADIR ESTO ARRIBA DE find_package
if(DEFINED ENV{GEODE_SDK})
    list(APPEND CMAKE_PREFIX_PATH "$ENV{GEODE_SDK}")
    list(APPEND CMAKE_MODULE_PATH "$ENV{GEODE_SDK}/share/cmake/Geode")
endif()

# 2) AHORA SÍ BUSCAR GEODE
find_package(Geode REQUIRED)

setup_geode_mod(MyCustomMod)

add_geode_sources(MyCustomMod
    src/main.cpp
)
