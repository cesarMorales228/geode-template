cmake_minimum_required(VERSION 3.13)

project(GeodeForgeTestMod)

include(${CMAKE_CURRENT_SOURCE_DIR}/cmake/Geode.cmake)

setup_geode_mod(GeodeForgeTestMod
    SOURCES
        src/main.cpp
)
