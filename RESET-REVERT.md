## `git reset`

**explicacion**

el comando git reset es una herramienta potente utilizada para deshacer cambios locales en git. su funcion principal es mover el puntero de la rama actual (head) a una confirmacion (commit) especifica, alterando el historial de tu repositorio y, opcionalmente, tu area de preparacion o directorio de trabajo.

**como funciona**

git administra tu proyecto a traves de tres componentes clave o "arboles":
historial de confirmaciones (head): el estado de tu proyecto hasta el ultimo commit.
area de preparacion (staging index): los archivos que has marcado con git add y que iran en el proximo commit.
directorio de trabajo: los archivos reales que ves y editas en tu carpeta.

**modos principales**

modo soft: mueve el puntero de tu rama al commit que especifiques. los cambios realizados en los commits posteriores se conservan y se envian directamente al area de preparacion (staging), dejandolos listos para que hagas un nuevo commit:
*git reset --soft hash-del-commit*

modo mixed: es el modo por defecto. mueve el puntero de tu rama al commit que elijas. ademas, elimina esos cambios del area de preparacion y los deja en tu directorio de trabajo (tendras que usar git add si quieres volver a prepararlos):
*git reset --mixed hash-del-commit*

modo hard: usalo con precaucion. mueve el puntero de tu rama al commit especificado, descarta todos los cambios intermedios en el area de preparacion y elimina las modificaciones en tu directorio de trabajo. tus archivos volveran al estado exacto del commit de destino y los cambios se perderan permanentemente:
*git reset --hard hash-del-commit*

deshacer un git add: si agregaste archivos por error con git add y quieres retirarlos sin perder los cambios en tu codigo, puedes ejecutar el comando apuntando al ultimo commit:
*git reset HEAD*

**precaucion**

dado que git reset reescribe el historial de confirmaciones, no debes usarlo en confirmaciones que ya hayas subido a un repositorio remoto si otras personas ya estan trabajando en el. para deshacer cambios en ramas publicas de forma segura sin alterar la historia, la alternativa correcta es utilizar git revert.
