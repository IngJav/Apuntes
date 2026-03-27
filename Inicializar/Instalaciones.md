# Aplicaciones
> INSTALACIÓN DE APLICACIONES

![C++](https://img.shields.io/badge/C%2B%2B-17%2B-00599C?logo=c%2B%2B&logoColor=white)
![g++](https://img.shields.io/badge/Compiler-g%2B%2B-blue)
![VSCode](https://img.shields.io/badge/VS%20Code-1E1E1E?logo=visual-studio-code)
![CodeBlocks](https://img.shields.io/badge/Code::Blocks-2E8B57)
![CLion](https://img.shields.io/badge/CLion-000000?logo=clion)
![Windows](https://img.shields.io/badge/Platform-Windows-0078D6?logo=windows&logoColor=white)

---
## Descripción General

Instructivo que sirve como guía en la instalación de ciertas aplicaciones

## Tabla de Contenido

- [Implementación Qt](#implementación-qt)
- [Características Principales](#características-principales)
- [Estructura de la Práctica](#estructura-de-la-práctica)
- [Interfaz del Sistema](#interfaz-del-sistema)
- [Tipos de Reportes](#tipos-de-reportes)
- [Ejecución del Programa](#ejecución-del-programa)
- [Agregar al PATH](#agregar-al-path)
---

## Implementación Qt
1. Utilizando La  Terminal

Se debe tener instalada la extensión `Qt C++ Extension pack`.
Se cuenta con dos compiladores para la creación de una aplicación con Qt

* `Proyecto1.pro`si se utiliza **qmake**. 
* `CmakeLists.txt`si se utiliza **cmake**  

En la carpeta principal correr los siguientes comandos
```bash
mkdir build
cd build
cmake .. 
cmake --build .
```
`cmake ..`configura el proyecto:
* Lee el archivo `CmakeLists.txt` 
* Revisa que compilador tiene
* Encuentra Qt y otras librerías necesarias
* Prepara los archivos de construcción
* Genera archivos para compilar, (`Makefile`, archivos Ninka y proyectos internos de build)
* Deja todo listo para compilar, más no compita totalmente.

`cmake --build .` utiliza la carpeta actual y funciona tipo: "usando los archivos de compilación que acabas de generar aquí mismo. Este comando sí compila el proyecto. Toma lo que preparó `cmake ..`y luego:
* Ejecuta el compilador
* Compila los `.cpp`
* Enlaza todo
* Genera el ejecutable final



Estructura **qmake**:
---
```bash
qt += core gui widgets

CONFIG += c++17 console
CONFIG -= app_bundle

TEMPLATE = app

SOURCES += \
    src/main.cpp \
    src/MainWindow.cpp \
    src/Token.cpp \
    src/LexicalAnalyzer.cpp \
    src/ErrorManager.cpp \
    src/ReporteGenerado.cpp \
    src/Paciente.cpp \
    src/Medico.cpp \
    src/Cita.cpp \
    src/Diagnostico.cpp \
    src/HospitalData.cpp \
    src/ParserBasico.cpp \

HEADERS += \
    src/MainWindow.h \
    src/Token.h \
    src/LexicalAnalyzer.h \
    src/ErrorManager.h \
    src/ReporteGenerado.h \
    src/Paciente.h \
    src/Medico.h \
    src/Cita.h \
    src/Diagnostico.h \
    src/HospitalData.h \
    src/ParserBasico.h \
```

Estructura **cmake**:
---
```bash
cmake_minimum_required(VERSION 3.16)

project(Proyecto1 VERSION 1.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTORCC ON)

find_package(Qt6 REQUIRED COMPONENTS Core Gui Widgets)

qt_standard_project_setup()

qt_add_executable(Proyecto1
    src/main.cpp
    src/MainWindow.cpp
    src/MainWindow.h
    src/Token.cpp
    src/Token.h
    src/LexicalAnalyzer.cpp
    src/LexicalAnalyzer.h
    src/ErrorManager.cpp
    src/ErrorManager.h
    src/ReporteGenerado.cpp
    src/ReporteGenerado.h
    src/Paciente.cpp
    src/Paciente.h
    src/Medico.cpp
    src/Medico.h
    src/Cita.cpp
    src/Cita.h
    src/Diagnostico.cpp
    src/Diagnostico.h
    src/HospitalData.cpp
    src/HospitalData.h
    src/ParserBasico.cpp
    src/ParserBasico.h
)

target_link_libraries(Proyecto1 PRIVATE
    Qt6::Core
    Qt6::Gui
    Qt6::Widgets
)

target_include_directories(Proyecto1 PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/src
)

if(WIN32)
    set_target_properties(Proyecto1 PROPERTIES
        WIN32_EXECUTABLE ON
    )
endif()
```












## Características Principales


## Estructura de la Práctica


## Interfaz del Sistema


## Tipos de Reportes:

## Ejecución del Programa

## Agregar al PATH
1. Presiona **Win + S**
2. Escribe: variables de entorno
3. Abre: Editar las variables de entorno del sistema
4. Entra a Variables de entorno
5. En "Variables del sistema", busca Path
6. Dale a Editar
7. Agrega una nueva ruta, por ejemplo se agregará Qt 

La dirección de instalación de Qt sería: `C:\Qt\Tools\CMake_64\bin`

![alt text](image-2.png)




