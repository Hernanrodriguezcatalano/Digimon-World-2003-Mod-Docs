# 02 - Extracción de la ISO y Archivos Base

Para modificar el juego, la imagen de CD (ISO, o BIN/CUE) debe ser desempaquetada. Un juego de PS1 no se edita directamente en su formato `.iso`, sino que se extraen sus componentes individuales (mapas, modelos, ejecutable) para ser modificados y luego reensamblados.

## Herramienta de Extracción Recomendada
El estándar actual para proyectos de PS1 (y el que es compatible con `mkpsxiso` y `zbuild`) es utilizar **dumpsxiso**. Esta herramienta de línea de comandos no solo extrae los archivos a la perfección, sino que genera un archivo XML con la estructura del disco, lo cual es vital para reconstruirlo después.

## Contenido Estándar Esperado
Al extraer *Digimon World 2003* (SLES_039.36 o similar), la carpeta `/workspace` debería contener:
* Archivo ejecutable principal (SLES / SLUS).
* `SYSTEM.CNF` (Archivo de configuración de arranque).
* Carpetas de datos (ej. `MAP/`, `BGM/`, `DAT/`, etc.).
