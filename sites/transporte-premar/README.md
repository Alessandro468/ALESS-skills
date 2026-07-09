# Transporte Premar — Landing

Landing page de una sola página para **Inversiones Premar 7879, C.A.** (RIF J-29893457-3),
transporte de carga refrigerada y seca en toda Venezuela.

Archivo único autónomo: [`index.html`](./index.html). Sin build ni dependencias.

## Diseño

- **Skills usadas:** `frontend-design` (dirección estética) + `ui-ux-pro-max` (paleta, tipografía, patrones UX).
- **Paleta:** Negro `#0B0B0C` + Rojo Premar `#D40F27` (del logo) + blanco/hueso.
  El cian `#1FB6D6` se usa **solo** para señalar la carga **refrigerada** (el color codifica el servicio, no decora).
- **Tipografía:** Archivo Expanded (display) · IBM Plex Sans (cuerpo) · IBM Plex Mono (datos), vía Google Fonts.
- **Firma visual:** la muesca negra de la "P" del logo, repetida como esquina achaflanada (clip-path)
  en botones y tarjetas; línea de ruta animada roja/cian.

## Datos a reemplazar (placeholders)

Busca y reemplaza en `index.html`:

| Placeholder | Aparece en | Reemplazar por |
|---|---|---|
| `584120000000` | enlaces `wa.me` y `tel:` | número real de WhatsApp/teléfono (formato internacional, sin `+` ni espacios) |
| `+58 412 000 0000` | tarjeta de contacto y footer | número visible real |
| `contacto@transportepremar.com` | contacto y footer | correo real |
| Estadísticas del hero (`20+`, `24/7`) | sección hero | cifras reales (años, estados, flota) |
| Lista de estados | sección Cobertura | estados donde realmente operan |

> El RIF `J-29893457-3` y la razón social ya están tomados del logo suministrado. Verifícalos.

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
