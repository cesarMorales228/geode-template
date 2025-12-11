cmake_minimum_required(VERSION 3.13)

project(GeodeForgeTestMod)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(GeodeForgeTestMod SHARED
    src/main.cpp
)

# Incluir headers del SDK que instala la action
if(DEFINED ENV{GEODE_SDK})
    target_include_directories(GeodeForgeTestMod PRIVATE
        $ENV{GEODE_SDK}/include
    )
else()
    message(FATAL_ERROR "GEODE_SDK env var is not set")
endif()

target_compile_definitions(GeodeForgeTestMod PRIVATE
    GEODE_MOD_ID="cesar.geodeforge.testmod"
)
