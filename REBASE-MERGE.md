## `git merge`

**explicacion**

basicamente, git merge es la herramienta que usas para juntar el historial y el trabajo de dos ramas distintas en una sola. es el comando estrella para agarrar todo lo que estuviste armando en tu rama aislada (por ejemplo, tu explicacion de los comandos) y meterlo por fin en la rama principal del proyecto (como la main).

**como usarlo en 4 simples pasos**

paso 1 - parate en la rama destino: te moves a la rama que va a recibir todo el trabajo nuevo (casi siempre es la main).
*git checkout main*

paso 2 - actualiza por las dudas: te traes lo ultimo del repositorio remoto por si algun compañero subio algo mientras vos trabajabas.
*git pull*

paso 3 - hace la fusion: le decis a git que traiga los cambios de la otra rama y los mezcle en la que estas parado ahora.
*git merge nombre-de-la-rama-que-quieres-unir*

paso 4 - subi los cambios: mandas el resultado final de la union a github para que quede guardado y lo vea el equipo.
*git push origin main*

**tipos de fusiones**

fast-forward (avance rapido): pasa cuando nadie toco la rama principal desde que vos creaste tu rama secundaria. es la mas facil, porque git simplemente avanza la rama actual hacia adelante para incluir tus commits nuevos. un tramite.

commit de merge: ocurre si tanto la rama principal como tu rama tuvieron cambios en paralelo. en este caso, git tiene que crear un "commit de union" especial que funciona como un puente para entrelazar los dos historiales.

**que pasa si hay conflictos**

si vos y un compañero modificaron exactamente la misma linea del mismo archivo, git levanta las manos, pausa el merge y te pide que lo resuelvas a mano porque no sabe que version priorizar. te va a tocar:
1. abrir el archivo en conflicto y borrar las marcas que te deja git, eligiendo a mano con que parte del codigo te quedas.
2. guardar el archivo ya limpio.
3. correr *git add .* y despues un simple *git commit* para terminar de sellar la fusion.
## `git rebase`

**explicacion**

el comando git rebase toma los commits de tu rama actual y los reanuda sobre el ultimo commit de otra rama, creando un historial lineal. en lugar de crear un commit de fusion (como git merge), reescribe el historial haciendo que parezca que desarrollaste tus cambios justo al final de la otra rama.

**para que sirve**

historial limpio: mantiene el registro de commits en una linea recta y facil de leer.
evitar commits de fusion: muy usado para actualizar tu rama de trabajo con los ultimos cambios de main sin añadir ruido al historial.

**regla de oro **

nunca utilices git rebase en ramas publicas o compartidas con otros desarrolladores en el servidor (como main o develop). al reescribir la historia, cambias los identificadores de los commits; si alguien mas ya descargo esos commits, su historial local chocara con el tuyo y causara problemas graves en el repositorio.

**ejemplo paso a paso**

imagina que tienes este escenario: tu rama main avanzo y tu rama feature se quedo atras. en lugar de mezclar todo y crear un commit adicional, puedes usar git rebase:

paso 1 - parate en tu rama feature:
*git checkout feature*

paso 2 - ejecuta el rebase:
*git rebase main*

git tomara todos tus cambios en feature, los guardara temporalmente, actualizara tu rama para que empiece en el punto mas reciente de main, y luego volvera a aplicar tus commits uno por uno al final.
