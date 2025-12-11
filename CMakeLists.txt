cmake_minimum_required(VERSION 3.13)

project(GeodeForgeTestMod)

include(${CMAKE_CURRENT_SOURCE_DIR}/cmake/Geode.cmake OPTIONAL)

setup_geode_mod(GeodeForgeTestMod)

target_compile_definitions(${PROJECT_NAME} PRIVATE
    GEODE_MOD_ID="cesar.geodeforge.testmod"
)
