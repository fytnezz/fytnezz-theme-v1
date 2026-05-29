# AGENTS

## Rol

Eres un agente de desarrollo para el tema Shopify de FYTNEZZ. Tu trabajo es mejorar fytnezz.com sobre una base Dawn, manteniendo versionado, calidad visual, rendimiento y seguridad comercial.

## Reglas principales

- Responde siempre en espanol al usuario.
- Trabaja sobre archivos reales del tema: `assets`, `config`, `layout`, `locales`, `sections`, `snippets`, `templates`.
- Antes de modificar una seccion Liquid importante, revisa los snippets y assets relacionados.
- No elimines configuraciones de `config/settings_data.json` sin confirmacion.
- No publiques cambios al tema live sin aprobacion explicita.
- Mantiene compatibilidad con Shopify Online Store 2.0.
- Prefiere cambios pequenos, probables y reversibles.
- Usa Dawn como referencia, pero adapta la experiencia a la marca FYTNEZZ.

## Calidad obligatoria

- Ejecuta `shopify theme check` cuando Shopify CLI este disponible.
- Revisa responsive: mobile, tablet y desktop.
- Mantiene accesibilidad basica: labels, contraste, foco visible, textos alternativos cuando aplique.
- Evita duplicar logica Liquid si ya existe un snippet reusable.
- Documenta cada cambio grande en el README o en notas de PR.

## Flujo Git recomendado

- `main`: rama conectada a Shopify solo cuando el cambio esta aprobado.
- `01_shopify_theme_active`: espejo del tema activo actual.
- `theme/fytnezz-live`: rama del tema publicado solo cuando se autorice.
- `theme/fytnezz-clean-v0`: version completa, funcional y no publicada.
- `lab/fytnezz-build-v0`: laboratorio de prueba.
- `feature/nombre-cambio`: rama de trabajo por modulo o arreglo.

## Prioridad de archivos

1. `sections`: estructura visible de paginas.
2. `snippets`: componentes reutilizables.
3. `assets`: CSS, JS, SVGs e imagenes.
4. `templates`: composicion JSON de paginas.
5. `config`: ajustes globales del tema.
6. `layout`: estructura global del HTML.
7. `locales`: traducciones y textos configurables.
