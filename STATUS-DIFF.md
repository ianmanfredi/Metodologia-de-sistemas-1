# Comandos de Estado y Cambios

## git status

**Qué hace y cuándo usarlo:** Muestra el estado actual del árbol de trabajo y del *staging area*. Usalo siempre antes de hacer un commit para confirmar exactamente qué archivos estás por guardar y cuáles aún no están rastreados.

**Cómo usarlo:**
1. Modificá o creá archivos en tu proyecto.
2. Abrí la terminal en la carpeta del repositorio.
3. Ejecutá el comando `git status`.
4. Revisá la salida: los archivos en verde están listos para el commit (*staged*), los rojos tienen cambios no preparados o no están rastreados.

---

## git diff

**Qué hace y cuándo usarlo:** Muestra las diferencias exactas de código línea por línea entre tu directorio de trabajo y el *staging area*. Usalo para revisar el detalle de tus modificaciones antes de ejecutar `git add`.

**Cómo usarlo:**
1. Modificá el contenido de un archivo que Git ya esté rastreando.
2. Ejecutá `git diff` en la terminal.
3. Analizá los resultados: las líneas con un `-` rojo fueron eliminadas, y las líneas con un `+` verde fueron agregadas.
4. Presioná la tecla `q` para salir de la vista de diferencias.