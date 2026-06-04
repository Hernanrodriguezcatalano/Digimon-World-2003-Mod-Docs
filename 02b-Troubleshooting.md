# Resolución de Problemas (Troubleshooting)

Registro de errores comunes encontrados durante la configuración del entorno y sus soluciones.

## Error en dumpsxiso: "File does not contain a valid ISO9660 file system"
**Causa:** La imagen de disco base está comprimida bajo el formato ECM (`.bin.ecm`). Las herramientas de extracción e inyección de PS1 no pueden leer sectores de datos comprimidos; requieren imágenes en formato raw/crudo (`.bin` o `.iso`).
**Solución:** 1. Obtener la utilidad `unecm`.
2. Arrastrar el archivo `.bin.ecm` sobre el ejecutable `unecm.exe` para decodificarlo.
3. Volver a ejecutar el comando de `dumpsxiso` apuntando al nuevo archivo `.bin` generado.
