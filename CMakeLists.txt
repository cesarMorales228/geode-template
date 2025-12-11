cmake_minimum_required(VERSION 3.13)

project(MyCustomMod)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Geode SDK: la acción exporta GEODE_SDK apuntando a la raíz del SDK.
# Dentro de eso suele estar GeodeConfig.cmake en:
#   $GEODE_SDK/lib/cmake/Geode
if(DEFINED ENV{GEODE_SDK})
    list(APPEND CMAKE_PREFIX_PATH "$ENV{GEODE_SDK}")
    list(APPEND CMAKE_MODULE_PATH "$ENV{GEODE_SDK}/lib/cmake/Geode")
endif()

find_package(Geode REQUIRED)

setup_geode_mod(MyCustomMod)

add_geode_sources(MyCustomMod
    src/main.cpp
)
