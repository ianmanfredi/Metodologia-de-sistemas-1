# Comandos de Historial y Trazabilidad

## git log

**Qué hace y cuándo usarlo:** Muestra el historial cronológico de los commits realizados en la rama actual. Usalo para ver la evolución del proyecto, buscar cuándo se introdujo una característica, o identificar el autor y el *hash* de un commit.

**Cómo usarlo:**
1. Posicionate en la rama de la que querés ver el historial.
2. Ejecutá `git log` en la terminal.
3. Usá las flechas del teclado o la barra espaciadora para navegar por la lista de commits.
4. Presioná `q` para salir del registro.

---

## git show

**Qué hace y cuándo usarlo:** Muestra la información detallada (autor, fecha, mensaje) y los cambios exactos de código (diff) de un commit en particular. Usalo cuando necesites analizar con precisión qué hizo un compañero en un commit específico.

**Cómo usarlo:**
1. Buscá el *hash* del commit que te interesa usando `git log` (ej. `a1b2c3d`).
2. Ejecutá `git show a1b2c3d`.
3. Revisá los metadatos del commit y las líneas de código que se agregaron o eliminaron.
4. Presioná `q` para volver a la línea de comandos.

---

## git reflog

**Qué hace y cuándo usarlo:** Muestra un registro de cada vez que se movió el puntero `HEAD`, incluyendo acciones que no aparecen en el historial normal (como *resets* o commits eliminados). Usalo como salvavidas si borraste algo por error o perdiste un commit y necesitás recuperarlo.

**Cómo usarlo:**
1. Ejecutá `git reflog` inmediatamente después de cometer un error crítico (como un mal *reset*).
2. Buscá en la lista el estado anterior al error y copiá su *hash* corto (ej. `HEAD@{2}`).
3. Ejecutá `git reset --hard HEAD@{2}` para devolver el repositorio a ese estado exacto.