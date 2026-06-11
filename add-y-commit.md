
# Guardado local: git add y git commit
Su funcion es guardar archivos localmente. 

Primero usas **git add** para seleccionar que archivos queres preparar para agregarlos al repo. Despues usas **git commit** para guardar esos archivos preparados en el repositorio.

### Tipos de commits 
* **feat:** Para agregar una nueva funcionalidad, explicacon o archivo.
* **fix:** Para solucionar un error.
* **style:** Para cambios visuales que no alteran el contenido.
* **docs:** Para modificaciones  en la documentacion del proyecto.
* **revert:** Para deshacer los cambios de un commit anterior. 

**Ejemplos de uso:**
```bash
git add archivo.txt
git add .
git commit -m "feat(documentacion): agregar explicacion de add y commit"