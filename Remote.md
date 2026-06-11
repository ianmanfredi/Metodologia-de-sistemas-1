# `git remote`

**¿Qué hace?**

Cuando inicializamos un repositorio en nuestra computadora sin haberlo creado en la pagina de github, al querer hacerlo vamos a tener que conectar ambos para que cuando subamos cambios desde nuestra computadora, los suba también al repositorio en github, para esto se utiliza el link del repositorio, pero como es tedioso usar el link cada vez que queremos enviar cambios, lo que hace este comando es agendar con un alias al repositorio, usualmente el alias es ‘origin’. por lo que al pushear los cambios realizados solemos ver algo como “git push origin main” Lo que significa: empuja el código a la rama principal del contacto ‘origin’.

**Ejemplo de uso:**

```bash
git remote add origin https://github.com/ianmanfredi/Metodologia-de-sistemas-1.git
```