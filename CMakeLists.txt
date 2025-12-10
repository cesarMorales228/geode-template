cmake_minimum_required(VERSION 3.13)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(MyCustomMod)

# --- CORRECCIÓN CLAVE ---
# Si estamos en GitHub Actions, Geode se instala en una ruta específica.
# Intentamos detectarla o usar la variable de entorno.
if (DEFINED ENV{GEODE_SDK})
    list(APPEND CMAKE_PREFIX_PATH "$ENV{GEODE_SDK}")
endif()

# Intentar encontrar Geode
find_package(Geode REQUIRED)

setup_geode_mod(MyCustomMod)

add_geode_sources(MyCustomMod
    src/main.cpp
)

