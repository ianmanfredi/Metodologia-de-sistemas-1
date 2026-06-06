#Gestion de ramas y navegacion en git

## `git branch`

**explicacion**

en git una rama (o branch) es una linea de desarrollo independiente. funciona como un espacio de trabajo aislado que te permite experimentar, probar nuevas caracteristicas o corregir errores sin afectar ni romper el codigo principal del proyecto. una rama en git no es una copia completa de todos los archivos de tu proyecto, sino un puntero ligero y movil que apunta a un commit especifico, al realizar un commit, el puntero de la rama avanza automaticamente, definiendo asi el historial de tu trabajo

**comandos principales**
ver ramas: para ver todas las ramas que existen en tu repositorio(el resultado mostrara una lista con un asterisco () marcando la rama en la que estás trabajando actualmente), simplemente ejecuta:
*git branch*
crear nueva rama: para crear una rama sin moverte automaticamente a ella(si prefieres crear la rama y cambiar a ella inmediatamente en un solo paso, puedes utilizar git checkout -b nombre-de-la-rama o git switch -c nombre-de-la-rama), escribe:
*git branch nombreRama*
moverse entre ramas: para saltar de una rama a otra y cargar sus archivos en tu directorio de trabajo, puedes utilizar
*git checkout nombreRama*
eliminar rama: una vez que hayas terminado de usar una rama (y asegurándote de que sus cambios ya fueron unidos a la rama principal), puedes eliminarla con:
*git branch -d nombreRama*
