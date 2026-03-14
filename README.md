# Apuntes 
> Lenguajes Formales - Prácticas Iniciales - IPC 2

![C++](https://img.shields.io/badge/C%2B%2B-17%2B-00599C?logo=c%2B%2B&logoColor=white)
![g++](https://img.shields.io/badge/Compiler-g%2B%2B-blue)
![VSCode](https://img.shields.io/badge/VS%20Code-1E1E1E?logo=visual-studio-code)
![CodeBlocks](https://img.shields.io/badge/Code::Blocks-2E8B57)
![CLion](https://img.shields.io/badge/CLion-000000?logo=clion)
![Windows](https://img.shields.io/badge/Platform-Windows-0078D6?logo=windows&logoColor=white)

---
## Descripción General

Aplicación desarrollada en C++ que permite analizar el rendimiento académico de estudiantes mediante el procesamiento de archivos `.lfp`, generando reportes estadísticos dinámicos en formato HTML.

El sistema modela las entidades académicas principales (`Estudiante`, `Curso`, `Nota`) y realiza análisis comparativos, métricas de desempeño y agrupaciones por carrera y semestre.


## Tabla de Contenido

- [Requisitos Técnicos](#requisitos-técnicos)
- [Conocimientos Aplicados](#conocimientos-aplicados)
- [Características Principales](#características-principales)
- [Estructura de la Práctica](#estructura-de-la-práctica)
- [Interfaz del Sistema](#interfaz-del-sistema)
- [Tipos de Reportes](#tipos-de-reportes)
- [Ejecución del Programa](#ejecución-del-programa)
- [Error en Compilación](#error-en-compilación)

---

## Requisitos Técnicos

| Recurso                  | Detalle                                      |
|--------------------------|----------------------------------------------|
| Lenguaje                 | C++17 o superior                             |
| Compilador recomendado   | g++ (MinGW) / MSVC / Clang                   |
| IDE compatible           | VS Code / Code::Blocks / CLion               |
| Librerías utilizadas     | STL (`vector`, `map`, `algorithm`, `fstream`)|
| Tipo de aplicación       | Consola                                      |
| Sistema Operativo        | Windows / Linux                              |
| Formatos de entrada      | `.lfp`                                       |
| Formatos de salida       | `.html`                                      |


## Conocimientos Aplicados

- Programación Orientada a Objetos (POO) en C++

- Arquitectura modular basada en separación de responsabilidades

- Manejo eficiente de memoria mediante referencias y punteros

- Uso avanzado de la STL para:
  - Búsqueda
  - Agrupación
  - Ordenamiento
  - Cálculo estadístico

- Complejidad algorítmica en recorridos y análisis de datos

- Generación automatizada de reportes HTML con estructura dinámica

- Procesamiento y transformación de datos académicos


## Características Principales
- Interfaz de consola interactiva con validación de entrada y control de errores.
- Centralización de lógica en la clase `Sistema`, actuando como núcleo del sistema.
- Arquitectura tipo controlador donde `Menu.cpp` gestiona la interacción y `Sistema` procesa la lógica.

## Estructura de la Práctica
```
LFP_A_1S2026/
├── Practica1/
│   ├── CargarC.cpp
│   ├── CargarE.cpp
│   ├── CargarN.cpp
│   ├── Curso.h
│   ├── Estudiante.h
│   ├── Menu.cpp
│   ├── Nota.h
│   ├── Sistema.cpp
│   ├── Sistema.h
│   ├── Archivos/
│   │   ├── cursos.lfp
│   │   ├── estudiantes.lfp
│   │   └── notas.lfp
│   ├── Reporte_Cursos_Mayor_Reprobacion.html
│   ├── Reporte_Distribucion_Completa.html
│   ├── Reporte_Estadisticas_Por_Curso.html
│   ├── Reporte_Rendimiento_Estudiantes.html
│   └── Reporte_Top10_Mejores_Estudiantes.html
├── Documentación/
│   └── ...
└── README.md
```



## Interfaz del Sistema

El sistema cuenta con una interfaz de consola interactiva que permite:

- Seleccionar opciones mediante un menú estructurado.
- Validación robusta de entrada para evitar caracteres inválidos.
- Control de flujo mediante estructura `do-while`.
- Manejo de errores utilizando `cin.fail()` y limpieza del buffer.
- Ejecución modular de funcionalidades centralizadas en la clase `Sistema`.

El menú principal permite:

1. Cargar estudiantes
2. Cargar cursos
3. Cargar notas
4. Generar estadísticas por curso
5. Generar rendimiento por estudiante
6. Generar Top 10 mejores estudiantes
7. Generar cursos con mayor reprobación
8. Generar análisis académico por carrera
9. Salir del sistema




## Tipos de Reportes:

| Reporte                           | Descripción Principal                                                        |
|-------------------------------------------|------------------------------------------------------------------------------|
| Cursos con Mayor Reprobación              | Muestra los cursos con mayor porcentaje de estudiantes reprobados.           |
| Distribución Completa de Notas            | Presenta la distribución de todas las calificaciones por curso.              |
| Estadísticas por Curso                    | Estadísticas detalladas (promedio, máxima, mínima) de cada curso.            |
| Rendimiento de Estudiantes                | Resumen del desempeño académico de cada estudiante.                          |
| Top 10 Mejores Estudiantes                | Lista de los 10 estudiantes con mejor rendimiento general.                   |

## Ejecución del Programa

1. Clonar el repositorio:

```bash
git clone https://github.com/IngJav/LFP_A_1S2026.git
```

2. Abrir la Carpeta **LFP_A_1S2026/Práctica1**


3. Abre el documento:
   
   `Menu.exe`

4. Los reportes se mostrarán en la misma carpeta.
   
   `Practica1`

---
## Error en Compilación
Si se realiza alguna modificación al código y se tiene problema en la compilación, correr el siguiente código en la términal de la carpeta **LFP_A_1S2026**:

```bash
g++ Practica1/Menu.cpp Practica1/Sistema.cpp Practica1/CargarE.cpp Practica1/CargarN.cpp Practica1/CargarC.cpp -o Practica1/Menu.exe
```


```bash
dotnet new console -n MiProyecto
cd MiProyecto
dotnet run
```
