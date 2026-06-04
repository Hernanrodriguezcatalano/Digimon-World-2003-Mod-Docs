# 01 - Herramientas y Configuración del Entorno (Setup)

Para poder modificar y recompilar *Digimon World 2003*, necesitamos preparar nuestro espacio de trabajo y cumplir con los requisitos del motor `zbuild` del proyecto de descompilación `ddw3`.

## 1. Estructura de Carpetas Local
El entorno de trabajo en la PC debe tener una estructura limpia. La carpeta principal del proyecto contiene:
* `/iso_original`: Aquí guardamos una copia de seguridad intocable de la ISO/BIN original.
* `/licenses`: Contiene los archivos de arranque de Sony necesarios para compilar el juego.
* `/workspace`: Aquí extraeremos los archivos del juego para modificarlos.

## 2. Creación de Licencias (Requisito de zbuild)
El motor de compilación necesita tres archivos en la carpeta `licenses/`:
1. `psexe-eu.dat`: Archivo de texto sin salto de línea.
2. `psexe-na.dat`: Archivo de texto sin salto de línea.
3. `psx-bin.dat`: Archivo binario de 28 KB extraído de los primeros sectores de la ISO.

## 3. Herramientas Base Necesarias
* **Hex Editor (HxD):** Para leer memoria RAM y modificar valores hexadecimales.
* **Emulador (DuckStation):** Permite jugar y usar herramientas de desarrollador (RAM Search).
* **Extractor de ISO (CDmage / UltraISO):** Para desempaquetar el juego.
