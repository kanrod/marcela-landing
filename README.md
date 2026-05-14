# Landing — Marcela [Apellido]

Sitio web de marca personal. Listo para desplegar en Vercel.

## Estructura

```
.
├── index.html      # Página completa (HTML + CSS + JS embebido)
├── marcela.jpg     # Foto profesional (800×1067, ~105 KB)
└── README.md       # Este archivo
```

Stack: HTML estático + CSS vanilla + JS vanilla. Sin dependencias, sin build step. Tipografías cargadas desde Google Fonts (Fraunces + Manrope).

---

## Placeholders por reemplazar antes del lanzamiento

Buscar y reemplazar en `index.html`:

| Placeholder        | Reemplazar por                                                |
|--------------------|---------------------------------------------------------------|
| `[APELLIDO]`       | Apellido(s) de Marcela. Aparece en `<title>`, meta tags, alt de imagen, schema.org y logo. |
| `[TU-DOMINIO]`     | Dominio definitivo, ej. `marcelagomez.co`. Aparece en `og:image`. |
| `[CAL_URL]`        | URL del calendario de agendamiento (Cal.com, Calendly, o similar). Aparece en el CTA final. |

El número de WhatsApp `573124045679` ya está configurado. Si cambia, buscar y reemplazar (4 ocurrencias).

---

## Despliegue en Vercel (5 minutos)

### Paso 1 — Crear repositorio en GitHub

1. Entrar a https://github.com y crear cuenta si no se tiene.
2. Click en `+` arriba a la derecha → `New repository`.
3. Nombre sugerido: `marcela-landing`. Visibilidad: privado o público (da igual para deploy).
4. Click `Create repository`.

### Paso 2 — Subir los archivos

En la página del repo recién creado:
1. Click `uploading an existing file`.
2. Arrastrar los tres archivos (`index.html`, `marcela.jpg`, `README.md`).
3. Click `Commit changes`.

### Paso 3 — Conectar Vercel

1. Entrar a https://vercel.com → `Sign up` → elegir `Continue with GitHub`.
2. Autorizar el acceso de Vercel a GitHub.
3. En el dashboard de Vercel: `Add New...` → `Project`.
4. Buscar el repo `marcela-landing` → `Import`.
5. Vercel detecta que es un sitio estático. No tocar nada. Click `Deploy`.
6. Esperar ~30 segundos. La URL queda algo como `marcela-landing-xxxx.vercel.app`.

### Paso 4 — Dominio personalizado (opcional, recomendado)

1. Comprar dominio en Namecheap, GoDaddy, o GoDaddy Colombia. Recomendado: `.co` (~40.000 COP/año).
2. En Vercel: `Project Settings` → `Domains` → `Add` → escribir el dominio.
3. Vercel da los registros DNS (un A record y un CNAME). Configurarlos en el panel del proveedor del dominio.
4. SSL se aprovisiona solo, en minutos.

### Paso 5 — Cambios futuros

Cada vez que se haga `commit` en GitHub, Vercel redespliega automáticamente. Para cambiar copy: editar `index.html` desde la interfaz web de GitHub y guardar — Vercel hace el resto.

---

## Performance esperado

- Lighthouse Performance: 95-100
- First Contentful Paint: < 1 s
- Cumulative Layout Shift: 0
- Peso total de la página: < 250 KB (image + fonts + html)

## Compatibilidad

- Probado en Chrome, Firefox, Safari, Edge (últimas versiones)
- Responsive: ≥ 360 px de ancho
- Funciona sin JavaScript en modo degradado (animaciones se desactivan, todo lo demás operativo)

---

## Mejoras posibles (post-lanzamiento)

- Open Graph image dedicada (1200×630) para previsualización en redes sociales
- Google Analytics 4 + Microsoft Clarity (insertar tags antes de `</body>`)
- Sitemap.xml + robots.txt
- Migrar a Next.js / Astro cuando se quiera agregar blog o secciones dinámicas
- Acuerdo de tratamiento de datos personales (si se agrega formulario que recolecte datos, exigido por la Ley 1581 de 2012 en Colombia)
