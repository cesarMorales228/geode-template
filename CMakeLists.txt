cmake_minimum_required(VERSION 3.13)

# Configuración básica
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Nombre del Proyecto (DEBE SER EL MISMO QUE EN MOD.JSON)
# En tu mod.json pusiste "id": "cesarMorales228.test_mod" (supongo) o "MyCustomMod"
# Aquí pon el nombre de la carpeta output
project(MyCustomMod)

# --- MAGIA PARA ENCONTRAR GEODE ---
# Si Geode no está en el PATH, intentamos configurarlo
list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake")

# Buscar Geode (Requerido)
find_package(Geode REQUIRED)

# Crear el Mod
setup_geode_mod(MyCustomMod)

# Archivos fuente
add_geode_sources(MyCustomMod
    src/main.cpp
)

# Opcional: Esto ayuda si usas Windows
if(MSVC)
	target_compile_options(MyCustomMod PRIVATE /utf-8)
endif()

