# FYTNEZZ Shopify Theme

Base local para modificar fytnezz.com usando Shopify Dawn, Codex PC, GitHub y la integracion de temas de Shopify.

## Estado actual

- Ruta activa local: `05_WEB/01_shopify_theme_active/fytnezz-shopify-theme`.
- Base tomada del tema activo local `01_shopify_theme_active`.
- Estructura Shopify valida: `assets`, `config`, `layout`, `locales`, `sections`, `snippets`, `templates`.
- Guias para agentes: `AGENTS.md`, `CODEX.md`, `.agents/skills`.
- GitHub conectado: cuenta `fytnezz`.
- Repo visible por el conector: `fytnezz/fytnezz-web-v5`.
- Pendiente tecnico: instalar o activar `git`, `gh` y Shopify CLI en Windows para subir el tema completo, crear ramas locales y sincronizar con Shopify sin hacerlo archivo por archivo.

## Fuentes base

- Dawn oficial en GitHub: https://github.com/Shopify/dawn
- Dawn en Shopify Theme Store: https://themes.shopify.com/themes/dawn
- Shopify CLI para temas: https://shopify.dev/docs/api/shopify-cli/theme
- Shopify GitHub integration: https://shopify.dev/storefronts/themes/tools/github

## Flujo recomendado

1. Instalar Git, GitHub CLI y Shopify CLI.
2. Usar o renombrar el repo GitHub a `fytnezz-theme`.
3. Subir esta carpeta como primera version del repo.
4. En Shopify Admin, conectar primero un tema no publicado/de prueba a una rama estable.
5. Trabajar cambios en ramas de laboratorio y feature antes de tocar la rama conectada al tema publicado.
6. Probar con Shopify CLI:

```powershell
shopify theme dev --store fytnezz.com
shopify theme check
```

7. Publicar cambios solo despues de revision visual y validacion.

## Ramas recomendadas

- `main`: base estable del repo.
- `01_shopify_theme_active`: espejo del tema activo actual, solo referencia y recuperacion.
- `theme/fytnezz-live`: rama para tema publicado cuando se autorice.
- `theme/fytnezz-clean-v0`: version completa, funcional y no publicada.
- `lab/fytnezz-build-v0`: laboratorio de prueba para home v0.
- `feature/fytnezz-home-v0`: desarrollo de la nueva home.
- `feature/*`: arreglos o modulos todavia no listos.

Ver detalles en `docs/REPOSITORY_STRATEGY.md`.

## Primer modulo de trabajo

La primera construccion sera la home page:

- header transparente limpio con logo #1
- header sticky al hacer scroll con blur oscuro/color editable y logo #2
- picker wheel
- utility panel
- aparicion/desaparicion de scrollbar
- home hero
- seccion colecciones
- philosophy grid + newsletter
- coverflow de cards Univerzo Hub
- footer con el mismo sistema visual del header
- controles editables desde Shopify Theme Editor cuando corresponda

Ver brief en `docs/HOMEPAGE_BUILD_BRIEF.md`.

## Datos que faltan para completar la conexion remota

- Confirmar si el repo remoto final sera `fytnezz/fytnezz-theme` o si debo usar `fytnezz/fytnezz-web-v5`.
- Confirmar que Shopify conectara un tema no publicado a `theme/fytnezz-clean-v0` o `lab/fytnezz-build-v0`.
- Instalar o exponer `git`, `gh` y `shopify` CLI en el PATH de Windows.
