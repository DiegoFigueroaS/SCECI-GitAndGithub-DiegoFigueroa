
# Buenas prácticas con commits y ramas en Git

## Escribir buenos commits

1. **Usar el verbo imperativo** como `Add`, `Fix`, `Change`, `Remove`
2. **Evitar puntuaciones innecesarias**
3. **Limitar a 50 caracteres el mensaje principal**
4. **Agregar contexto en el cuerpo del commit**
5. **Usar prefijos como `feat`, `fix`, `docs`**

## Nombres de rama

- bug/fix-error
- feature/new-login
- experiment/test-ui
- hotfix/quick-patch

### Agrega IDs si usas JIRA
Ejemplo: `123-feature/new-login-page`

## Uso de herramientas para mejorar los commits

Instala Husky y Commitlint para revisar tests o convenciones antes de hacer push:

```bash
npm install husky --save-dev
npx husky install
npx husky add .husky/pre-push "npm test"
```

## Reescribir historial: cuidado

Solo se recomienda si expusiste información sensible. Usa `git revert` mejor si solo fue un error de código.

## ¿Cuándo hacer commit?

Haz commits pequeños y frecuentes. Como decía Julio César: *divide y vencerás*.