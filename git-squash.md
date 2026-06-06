
# Limpieza de historial: "Squash"

**squash** no es un comando, sino una instruccion que le damos a git.
Su funcion es fusionar  varios commits chicos  para convertirlos en uno solo limpiando el historial. 

### Ejemplo de uso:
```bash
git rebase -i HEAD~3

```

Al ejecutarlo, Git abre el editor de texto donde podes cambiar la palabra "pick" por "squash" en los commits que queres fusionar.
```
pick hash1 "hola 1"
squash hash2 "hola 12"
squash hash3 "hola 123"
```
Al guardar y cerrar el editor, esos tres commits forman uno solo.