# Commits, Staging y Restauración

## ¿Qué es un commit?
Un commit es como una foto del proyecto en un momento específico, guarda todos los cambios y los deja registrados con autor, fecha, etc. 

## Área de staging
Cuando modificamos un archivo, primero lo tenemos en estado modificado. Si queremos guardarlo, primero lo pasamos al área de staging (temporal), con `git add`, y luego lo confirmamos con `git commit`.

## Comandos útiles

- `git commit`: abre el editor para escribir un mensaje.
- `git commit -m "mensaje"`: crea un commit directo con mensaje.
- Se pueden usar varios `-m` para título y descripción.

## Restaurar archivos

- Si agregaste un archivo por error al staging:  
  `git reset <archivo>` → lo saca del staging.

- Si ya estaba en el repositorio y lo modificaste pero quieres volver atrás:  
  `git restore <archivo>`  
  `git restore .` → todos los archivos.

## Estados posibles de un archivo

1. **Modificado**: cambió, pero no está en staging.
2. **Preparado (staged)**: listo para commit.
3. **Confirmado (committed)**: ya guardado en el repositorio.

## ¿Qué es HEAD?
HEAD es como un "estás aquí" del historial. Siempre apunta al último commit que estás viendo o modificando.

