
# `git fetch`

**¿Qué hace?**

Lo que hace este comando es ver si otro integrante del repositorio ha subido cambios. Este comando descarga a tu computadora la información de los cambios que subieron otros integrantes, pero de forma segura, ya que no une ni modifica los archivos en los que estás trabajando actualmente.

**Ejemplo de uso:**

```bash
git fetch origin
```


# `git pull`

**¿Qué hace?**

Hace casi lo mismo que fetch, va a ver si hay cambios o no, solo que este comando une directamente los cambios a tu version del trabajo. Si alguien habia modificado algo este comando te va a unir esos cambios, por lo que hay que tener cuidado por si había una modificación en los mismos archivos en los que estabas trabajando ya que eso podría causar conflictos que deberías luego arreglar a mano.

**Ejemplo de uso:**
```bash
git pull origin main
```
