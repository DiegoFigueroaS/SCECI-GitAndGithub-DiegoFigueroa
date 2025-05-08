# Estrategias de Desarrollo con Git: Trunk Based y Git Flow

## Git Flow

Git Flow es una estrategia pensada pa equipos grandes o medianos ke necesitan tener un orden al momento d trabajar en features, arreglos y lanzamientos.

### Ramas principales

- **main (o master)**: contien el codigo final ke se sube a produccion
- **develop**: es la rama base para nuevas features o cambios ke aun no estan listos pa subir a produccion

### Ramas de apoyo

- **Feature**: se crean desde `develop` y se fusionan a `develop`
- **Release**: salen de `develop` y se fusionan en `main` y `develop`
- **Hotfix**: vienen de `main` para arreglar algo urgente y vuelven a `main` y `develop`

### Reglas de fusion

Pa ramas feature y release se suele usar `--no-ff` pa mantener historial claro. Esto ayuda a saber ke cambios vinieron d donde.

## GitHub Flow

Este flujo es mas simple y directo. Pensado pa equipos ke lanzan seguido.

- se crea una rama desde `main`
- se trabaja ahi hasta ke este listo
- se hace una PR
- se revisa se testea y se sube

Aki todo gira entorno a PRs ke se discuten antes d subir a main

## Trunk Based Development

Este enfoque es pa equipos ke integran a `main` (o `trunk`) seguido. No hay muchas ramas ni ramas largas. Todos trabajan sobre `main` o ramas ke duran un par de dias maximo.

- Commits pekeños y constantes
- se sube y testea todo el tiempo
- se integra lo mas rapido posible
- idealmente hay CI/CD configurado

## Ship Show Ask y flujos de trabajo en Git

## Estrategias de ramas rapidas

Esta estrategia esta buena pa cuando uno quiere mover cambios rapido y no perderse tanto en el review
El truco ta en saber bien que tipo de cambio estas haciendo y en base a eso usar una estrategia distinta

## Tipos de estrategias

- **Ship**: vas directo al main sin esperar revisiones ni nada. Asegurate que todo esta bien antes, no seas loco.
- **Show**: haces PR pa que pase por CI pero no esperas que alguien lo mire, solo quieres asegurarte que los tests no rompan.
- **Ask**: aqui si esperas que alguien del equipo te ayude. Hay dudas, cosas medias raras, mejor preguntar.

## Cuándo usar cada una

### Ship

Pensado pa:
- cambios pequeños que ya sabes que funcionan
- arreglos simples
- docu que se te paso
- mejoras de estilo que no afectan lógica
- agregar tests nuevos

### Show

Útil cuando:
- confias en lo que hiciste pero igual queres pasar por CI
- queres que quede registro del cambio
- no esperas feedback de nadie, solo validacion tecnica

### Ask

Para:
- cambios grandes o raros
- cosas que no sabes si van a funcionar bien
- donde hay riesgo o no estas seguro
- queres tener una charla antes de mergear

## Trucos pa no romper nada

- siempre hacé commits chicos y seguidos
- no te guardes ramas por mucho tiempo, max 2 o 3 dias
- avisá si vas a mergear algo con dudas
- usá feature flags si todavia no esta todo cerrado
- si algo rompe, reverti rapido

### Consideraciones

- Tener buena cobertura d test
- usar lint
- trabajar en parejas

Es una forma agresiva pero eficiente d mantener el repo limpio y activo sin mucho drama.
