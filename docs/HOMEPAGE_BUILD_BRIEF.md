# FYTNEZZ Homepage Build Brief

## Objetivo

Construir la home page v0 de FYTNEZZ sobre Dawn, con una experiencia luxury-performance, cinematografica, mobile-first, modular y editable desde Shopify Theme Editor.

## Referencias locales

- Tema activo: `05_WEB/01_shopify_theme_active/fytnezz-shopify-theme`
- Referencia visual/textual: `Carpeta sin titulo`
- Referencia frontend principal: `Carpeta sin titulo/FYTNEZZ FRONTEND.txt`

## Estructura inicial de la home

1. Header
2. Home hero
3. Seccion colecciones
4. Univerzo Hub coverflow
5. Philosophy grid + newsletter
6. Footer

## Header

Estado inicial:

- transparente/limpio
- logo #1
- navegacion premium
- iconos lineales
- sin fondo pesado

Estado scroll:

- sticky
- blur oscuro
- color personalizable
- logo #2
- divider fino
- transicion suave

Controles deseables:

- logo inicial
- logo sticky
- color de fondo sticky
- opacidad
- blur
- color de links
- color hover
- altura desktop
- altura mobile
- mostrar/ocultar iconos

## Home Hero

Debe ser primera vista real de marca, no landing generica.

Requisitos:

- fondo visual fuerte o media editable
- composicion editorial
- headline corto
- CTA principal y secundario editables
- mobile-first
- sin exceso de cards flotantes

## Colecciones

Requisitos:

- tarjetas premium
- imagen editable por bloque
- titulo, subtitulo y link editables
- layout responsive
- hover sutil

## Univerzo Hub Coverflow

Requisitos:

- cards con profundidad visual controlada
- navegacion fluida
- soporte touch/mobile
- texto legible
- controles editables
- no romper scroll de pagina

## Picker Wheel

Uso previsto:

- selector visual de universo, categoria o experiencia.
- debe ser controlado y accesible.
- no debe secuestrar scroll.

## Utility Panel

Uso previsto:

- panel lateral o flotante para acciones utiles.
- comportamiento configurable.
- abrir/cerrar con transiciones suaves.

## Scrollbar

Objetivo:

- aparicion/desaparicion elegante sin bloquear scroll.
- corregir problemas de scroll existentes en fytnezz.com.

Regla:

- nunca usar scripts que bloqueen wheel/touchmove globalmente salvo en modales activos y con escape claro.

## Philosophy Grid + Newsletter

Requisitos:

- grid editorial brutalista premium
- textos configurables
- newsletter integrado con Dawn/Shopify
- no parecer bloque generico

## Footer

Debe compartir sistema visual con header:

- fondo oscuro editable
- blur o superficie premium si aplica
- links organizados
- newsletter o social si corresponde
- iconos editables
- spacing responsive

## Archivos probables

- `sections/header.liquid`
- `sections/footer.liquid`
- `sections/fytnezz-home-hero.liquid`
- `sections/fytnezz-collections-showcase.liquid`
- `sections/fytnezz-univerzo-coverflow.liquid`
- `sections/fytnezz-philosophy-newsletter.liquid`
- `assets/fytnezz-theme.css`
- `assets/fytnezz-theme.js`
- `templates/index.json`

## Validacion

- Shopify Theme Editor carga sin errores.
- Home funciona en mobile, tablet y desktop.
- Scroll natural funciona.
- Header cambia correctamente al hacer scroll.
- No hay texto cortado ni superpuesto.
- No hay errores JS en consola.
- `shopify theme check` pasa cuando Shopify CLI este disponible.

