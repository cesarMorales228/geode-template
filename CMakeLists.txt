cmake_minimum_required(VERSION 3.13)

project(GeodeForgeTestMod)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Incluir nuestro wrapper, que a su vez incluye el del SDK en Actions
include(${CMAKE_CURRENT_SOURCE_DIR}/cmake/Geode.cmake OPTIONAL)

setup_geode_mod(GeodeForgeTestMod)

add_geode_sources(GeodeForgeTestMod
    src/main.cpp
)
