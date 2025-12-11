cmake_minimum_required(VERSION 3.13)

project(GeodeForgeTestMod)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(GeodeForgeTestMod SHARED
    src/main.cpp
)

# No tocamos include dirs ni nada;
# el action ya pasa -I al SDK cuando llama a CMake.
target_compile_definitions(GeodeForgeTestMod PRIVATE
    GEODE_MOD_ID="cesar.geodeforge.testmod"
)
