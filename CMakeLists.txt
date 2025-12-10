cmake_minimum_required(VERSION 3.13)
set(CMAKE_CXX_STANDARD 20)

# Nombre de tu proyecto (debe coincidir con mod.json si es posible)
project(MyCustomMod)

# Importar Geode
find_package(Geode REQUIRED)

# Crear el binario con tu código fuente
setup_geode_mod(MyCustomMod)

# Añadir tus archivos C++ (Asegúrate de que existan)
add_geode_sources(MyCustomMod
    src/main.cpp
)
