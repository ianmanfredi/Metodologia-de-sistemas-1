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


## `git checkout`

**explicacion**

el comando git checkout se utiliza principalmente para navegar entre diferentes ramas, restaurar archivos del directorio de trabajo o explorar puntos especificos en el historial de confirmaciones (commits). Basicamente le indica a git que actualice los archivos de tu proyecto para que coincidan con la version exacta de la entidad seleccionada

cambiar rama: Permite saltar entre distintas líneas de trabajo (ramas). Cuando cambias de rama, Git modifica automáticamente todos los archivos de tu carpeta para que reflejen el estado en el que quedó esa rama
*git checkout nombreRama*
moverse a un commit especifico: Puedes usar checkout para viajar en el tiempo y ver exactamente cómo era tu código en un commit específico. Esto mueve tu puntero HEAD a un estado conocido como detached HEAD:
*git checkout idCommit*
restaurar archivos:Si has realizado cambios en un archivo local pero decides que quieres descartarlos y volver a la versión guardada en el último commit, puedes usar checkout para extraer ese archivo de nuevo.:
*git checkout -- nombreArchivo*

Nota: Si utilizas una versión moderna de Git, los comandos git switch (para cambiar de rama) y git restore (para restaurar archivos) han ido reemplazando paulatinamente a git checkout para evitar confusiones, ya que checkout englobaba demasiadas funciones diferentes
