# Transporte Premar — Sitio web

Sitio multipágina para **Inversiones Premar 7879, C.A.** (RIF J-29893457-3),
transporte de carga refrigerada y seca en toda Venezuela. Sin build ni dependencias.

## Páginas

| Archivo | Menú | Contenido |
|---|---|---|
| `index.html` | Inicio | Hero, resumen de servicios, diferenciales, CTA |
| `servicios.html` | Servicios | Detalle de carga refrigerada, seca y distribución (con espacios para fotos) |
| `cobertura.html` | Cobertura | Estados con servicio y ejes de ruta |
| `flota.html` | Flota | Unidades y especificaciones |
| `proceso.html` | Proceso | Pasos 01–04, de la cotización a la entrega |
| `contacto.html` | Contacto | WhatsApp, teléfonos, correo y datos de la empresa |

CSS compartido en `assets/styles.css`; fotos en `assets/fotos/`.
El menú superior y el footer enlazan estas páginas; la página activa se resalta en rojo.

## Diseño

- **Skills usadas:** `frontend-design` (dirección estética) + `ui-ux-pro-max` (paleta, tipografía, patrones UX).
- **Paleta:** Negro `#0B0B0C` + Rojo Premar `#D40F27` (del logo) + blanco/hueso.
  El cian `#1FB6D6` se usa **solo** para señalar la carga **refrigerada** (el color codifica el servicio, no decora).
- **Tipografía:** Archivo (display, peso 900) · IBM Plex Sans (cuerpo) · IBM Plex Mono (datos), vía Google Fonts.
- **Firma visual:** la muesca negra de la "P" del logo, repetida como esquina achaflanada (clip-path)
  en botones y tarjetas; línea de ruta animada roja/cian.

## Datos cargados

- **WhatsApp:** +58 414 303 8227 (Venezuela) · enlaces `wa.me/584143038227`
- **Teléfono (USA):** +1 786 210 5098 · `tel:+17862105098`
- **Correo:** inversionespremar@gmail.com
- **Frío controlado:** −18°C a +8°C (hero, servicios y flota)
- **Empresa / RIF:** Inversiones Premar 7879, C.A. — RIF J-29893457-3

## Pendiente por confirmar (placeholders)

| Placeholder | Aparece en | Reemplazar por |
|---|---|---|
| Estadísticas del hero (`20+`, `24/7`) | sección hero | cifras reales (estados cubiertos, disponibilidad) |
| Lista de estados | sección Cobertura | estados donde realmente operan |

> El RIF y la razón social se tomaron del logo suministrado. Verifícalos.

## Desplegar

Cualquier hosting de estáticos sirve. Ejemplos:

```bash
# Netlify (arrastrar la carpeta) o CLI:
netlify deploy --dir=sites/transporte-premar --prod

# Vercel:
vercel deploy sites/transporte-premar

# GitHub Pages: publicar el contenido de esta carpeta.
```

Requiere conexión a internet del visitante para cargar las fuentes de Google Fonts.
Para funcionamiento 100% offline, se pueden auto-alojar las fuentes (woff2) y ajustar el `@import`.
