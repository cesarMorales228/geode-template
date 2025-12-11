cmake_minimum_required(VERSION 3.13)

project(GeodeForgeTestMod)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(GeodeForgeTestMod SHARED
    src/main.cpp
)

target_include_directories(GeodeForgeTestMod PRIVATE
    $ENV{GEODE_SDK}/include
    ${CMAKE_CURRENT_SOURCE_DIR}/geode-sdk-clone/include
)

target_compile_definitions(GeodeForgeTestMod PRIVATE
    GEODE_MOD_ID="cesar.geodeforge.testmod"
)
