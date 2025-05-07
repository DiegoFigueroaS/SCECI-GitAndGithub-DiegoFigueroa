# Ramas en Git

## ¿Qué es una rama?

Una rama es como una copia del proyecto donde puedes trabajar sin afectar la rama principal. Es útil para desarrollar nuevas ideas, probar cosas o hacer cambios sin romper nada. Después se puede juntar con el trabajo principal (la rama main).

En equipos, cada quien trabaja en su rama y al final se integran (si todo va bien). Esto ayuda a organizar el trabajo y no pisarse entre todos.

> Ejemplo visual (ver imagen en `assets/branches.png`)

## Crear, cambiar y borrar ramas

- Crear una rama: `git branch mi-rama`
- Cambiar a la rama: `git switch mi-rama`
- Crear y cambiar al mismo tiempo: `git switch -c mi-rama`
- Ver rama actual: `git branch --show-current`

Si la quieres borrar:

- Si ya fue fusionada:
  `git branch -d mi-rama`
- Si no fue fusionada (a la fuerza):
  `git branch -D mi-rama`

Git no deja borrar una rama sin fusionar para evitar que pierdas trabajo.

## ¿Qué es un merge?

El `merge` sirve para juntar los cambios de una rama con otra. Lo normal es estar en la rama `main` y correr:

```bash
git merge mi-rama
```

Esto mete los cambios de `mi-rama` en `main`. Pero si hubo cambios en las mismas líneas de un archivo, vas a tener un conflicto.

## ¿Qué es un conflicto?

Un conflicto pasa cuando Git no sabe qué cambio mantener entre dos ramas. Te pone marcas en el archivo:

```diff
<<<<<<< HEAD
código que estaba en main
=======
código que viene de la otra rama
>>>>>>> changes
```

Tienes que elegir con qué parte quedarte o unir ambas. Después de resolverlo, haces `git add archivo` y terminas con un commit.

> Ver imagen ilustrativa en `assets/conflict.png`

## Consejos rápidos

- Siempre verifica que una rama fue mergeada antes de borrarla.
- Lee los conflictos con calma antes de resolver.
- Usa `git diff` para entender mejor los cambios.