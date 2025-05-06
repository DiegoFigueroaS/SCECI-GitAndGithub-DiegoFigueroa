# Control de versiones y fundamentos de Git

## ¿Qué es un control de versiones?
Es un sistema que guarda cada cambio que se hace en los archivos de un proyecto. Así puedes saber quién hizo qué y cuándo, y tener un historial completo del código.

## Fundamentos de Git
- Todo gira alrededor de los repositorios.
- Un repo puede ser local (en tu compu) o remoto (en GitHub, por ejemplo).
- Los cambios se pueden integrar con otras ramas usando `merge`.
- Para subir los cambios al remoto se usa `push`, y para traerlos de vuelta, `pull`.

## Configuración de Git
Antes de usar Git hay que configurar tu nombre y correo:

```bash
git config --global user.name "Tu nombre"
git config --global user.email "tu@email.com"
