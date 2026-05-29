# FYTNEZZ Repository Strategy

## Cuenta GitHub

- Cuenta: `fytnezz`
- Repo recomendado: `fytnezz-theme`
- Repo visible actualmente por el conector: `fytnezz/fytnezz-web-v5`

GitHub no usa espacios en nombres de repo. Por eso `fytnezz theme` debe convertirse en `fytnezz-theme`.

## Ramas

### `main`

Rama base estable del repositorio. No debe conectarse directamente al tema live hasta que el flujo este probado.

### `01_shopify_theme_active`

Espejo del tema activo actual. Sirve para recuperar el estado original de fytnezz.com.

Reglas:

- No experimentar aqui.
- Solo actualizar cuando se haga un pull/export verificado desde Shopify.
- No conectar a un tema de prueba si se va a modificar fuerte.

### `theme/fytnezz-live`

Rama para el tema publicado de fytnezz.com cuando el usuario autorice publicacion.

Reglas:

- Solo recibe merges desde ramas limpias y probadas.
- No se trabaja directo aqui.

### `theme/fytnezz-clean-v0`

Version completa, funcional, sin errores conocidos y no publicada. Esta es la mejor rama para conectar a un tema no publicado de prueba en Shopify.

### `lab/fytnezz-build-v0`

Laboratorio para construir la primera version de la home. Puede romperse mientras se esta desarrollando.

### `feature/fytnezz-home-v0`

Rama de desarrollo enfocada en la home page:

- header
- home hero
- colecciones
- philosophy grid
- newsletter
- Univerzo Hub coverflow
- footer
- controles del Theme Editor

### `feature/*`

Ramas para modulos incompletos, arreglos, pruebas visuales o experimentos.

Ejemplos:

- `feature/header-transparent-sticky`
- `feature/utility-panel`
- `feature/picker-wheel`
- `feature/univerzo-coverflow`
- `feature/footer-system`

## Repositorios por version

Si quieres separar versiones como repos distintos:

- `fytnezz-build-v0`: primer build experimental.
- `fytnezz-build-v1`: primera version candidata.
- `fytnezz-theme`: repo principal limpio.

Recomendacion tecnica: usar un solo repo `fytnezz-theme` con tags y ramas. Crear repos por version solo para snapshots o archivos historicos.

## Shopify connection

Para empezar:

- Conectar un tema no publicado a `theme/fytnezz-clean-v0`.
- Usar `lab/fytnezz-build-v0` solo para pruebas internas si Shopify permite seleccionar esa rama como tema separado.
- No conectar `theme/fytnezz-live` hasta que la home este validada.

## Bloqueos tecnicos actuales

En este PC no aparecen disponibles:

- `git`
- `gh`
- `shopify`

Sin esas herramientas se puede preparar el codigo local, pero no se puede hacer el flujo completo normal de branch, commit, push y theme check desde Codex.

