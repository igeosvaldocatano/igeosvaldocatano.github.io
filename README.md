# Landing Page — EOCC Consultoría Independiente

Página web de presentación personal y de marca para **Edgar Osvaldo Cataño Castillo**, consultor independiente en Gestión Empresarial. Archivo HTML autónomo, sin dependencias externas ni frameworks, listo para abrir en cualquier navegador o publicar en cualquier servicio de hosting.

---

## Descripción general

La landing page funciona como carta de presentación digital de EOCC. Está construida en un solo archivo HTML que incluye todos los estilos, imágenes y fuentes incrustadas (en base64), lo que significa que no requiere conexión a internet para mostrar el contenido visual — solo carga la tipografía Montserrat / Open Sans desde Google Fonts si hay red disponible.

**Tagline:** *"Claridad operativa. Resultados reales."*

---

## Características principales

- **Navbar fija** con navegación interna a cada sección y botón de contacto destacado
- **Hero de pantalla completa** con logo, nombre, tagline y dos llamadas a la acción
- **Barra de estadísticas** — 12+ años, 15+ empresas, 100+ procesos implementados, 10 servicios
- **Sección Acerca de** con foto de perfil, descripción, valores de marca y tarjeta interactiva de CV
- **Modal de perfil profesional** con experiencia, formación, áreas de expertise y sectores atendidos
- **Los 8 síntomas de la PyME estancada** — sección diagnóstico basada en la presentación de primer contacto
- **Catálogo de 12 tarjetas de servicios** — 11 servicios específicos + 1 tarjeta de contacto abierto
- **Sección de metodologías** organizadas por categoría (Procesos, Calidad, Mejora Continua, Auditoría, IA)
- **4 modelos de contratación** — Iguala mensual, Por proyecto, Por hora/sesión, Capacitaciones
- **Sección "¿Para quién es EOCC?"** con checklist del cliente ideal y diferenciadores vs. firmas grandes
- **Sección de contacto** con botones directos a WhatsApp, teléfono, correo e Instagram
- **Diseño responsivo** adaptado a móvil y escritorio
- **Identidad visual EOCC** aplicada al 100%: paleta de colores, tipografía Montserrat, logo y foto incrustados

---

## Paleta de colores

| Nombre       | Hex       | Uso principal                        |
|--------------|-----------|--------------------------------------|
| Azul Marino  | `#0E4576` | Color primario, bordes, navbar       |
| Azul Noche   | `#1E3347` | Fondos oscuros, hero, modal          |
| Marfil       | `#F0EBE0` | Fondo claro, texto sobre oscuro      |
| Ámbar Dorado | `#C4933F` | Botones principales, labels          |
| Mostaza      | `#F4A925` | Acentos, líneas decorativas, números |

---

## Cómo abrir el archivo

1. Localiza el archivo `Landing_EOCC.html` en la carpeta del proyecto
2. Haz doble clic — se abre directamente en tu navegador predeterminado
3. No requiere servidor local, instalación de software ni conexión a internet para funcionar

Para compartirlo digitalmente puedes enviarlo por correo, subirlo a Google Drive, Dropbox o cualquier servicio de almacenamiento en la nube y compartir el enlace de descarga.

---

## Cómo publicarlo en línea

Para que la página tenga una URL pública puedes usar cualquiera de estas opciones gratuitas:

**Opción A — GitHub Pages**
1. Crea un repositorio en [github.com](https://github.com)
2. Sube `Landing_EOCC.html` y renómbralo como `index.html`
3. Ve a *Settings → Pages* y activa GitHub Pages desde la rama `main`
4. Tu página estará disponible en `https://tu-usuario.github.io/nombre-repo`

**Opción B — Netlify Drop**
1. Entra a [app.netlify.com/drop](https://app.netlify.com/drop)
2. Arrastra el archivo `Landing_EOCC.html` a la zona de carga
3. Netlify genera una URL pública al instante (puedes personalizar el subdominio)

**Opción C — Tiiny.host**
1. Ve a [tiiny.host](https://tiiny.host)
2. Sube el archivo y elige un nombre de subdominio
3. Obtén una URL compartible de inmediato, sin registro obligatorio

---

## Cómo personalalizarlo

Todos los textos y datos de contacto están en el cuerpo HTML del archivo. Puedes editarlo con cualquier editor de texto (VS Code, Notepad++, etc.).

### Datos de contacto
Busca en el HTML las siguientes cadenas y sustitúyelas si cambian:

```
ige.osvaldocatano@gmail.com   → tu nuevo correo
524445509700                  → número de WhatsApp (formato internacional sin +)
4445509700                    → número de teléfono para llamada directa
ige.osvaldocatano             → usuario de Instagram
```

### Foto de perfil
La foto está incrustada en base64 dentro del atributo `src` de la etiqueta `<img class="about-photo" ...>`. Para cambiarla:

1. Convierte tu nueva foto a base64 (puedes usar [base64.guru/converter/encode/image](https://base64.guru/converter/encode/image))
2. Localiza en el HTML la línea que empieza con `<img class="about-photo" src="data:image/jpeg;base64,`
3. Reemplaza el bloque base64 con el de tu nueva imagen

### Logo
El logo aparece en tres lugares: navbar, hero y footer. Todos comparten la misma imagen incrustada en base64. Busca `<img class="nav-logo"`, `<img class="hero-logo"` y `<img` dentro del `<footer>` para localizarlos.

### Tamaños del logo
| Elemento    | Clase CSS      | Tamaño actual |
|-------------|----------------|---------------|
| Navbar      | `.nav-logo`    | `height: 88px` |
| Hero        | `.hero-logo`   | `height: 360px` |
| Footer      | *(inline img)* | `height: 60px` |

### Servicios
Cada tarjeta de servicio es un `<div class="service-card">` dentro del grid `#services`. Puedes añadir, eliminar o modificar tarjetas siguiendo la misma estructura:

```html
<div class="service-card">
  <div class="service-num">XX</div>
  <div class="service-icon">🔧</div>
  <h4>Nombre del servicio</h4>
  <p>Descripción del servicio.</p>
  <span class="service-time">⏱ Tiempo estimado</span>
</div>
```

### Colores de marca
Las variables CSS están declaradas al inicio del bloque `<style>` bajo `:root { ... }`. Modificar un valor ahí actualiza el color en toda la página de forma automática.

---

## Estructura del archivo

```
Landing_EOCC.html
│
├── <head>          Metadatos, Google Fonts, bloque <style> completo
│
└── <body>
    ├── <nav>           Navbar fija con logo y menú
    ├── #hero           Sección principal (hero)
    ├── #stats          Barra de estadísticas
    ├── #about          Acerca de EOCC + foto + tarjeta CV
    ├── #cv-modal       Modal de perfil profesional (oculto por defecto)
    ├── #symptoms       Los 8 síntomas de la PyME estancada
    ├── #services       Catálogo de 12 tarjetas de servicios
    ├── #methodology    Metodologías por categoría
    ├── #models         Modelos de contratación
    ├── #market         ¿Para quién es EOCC?
    ├── #cta            Sección de contacto
    └── <footer>        Pie de página
```

---

## Contacto

**Edgar Osvaldo Cataño Castillo — EOCC**
Consultoría Independiente en Gestión Empresarial
San Luis Potosí, S.L.P., México

- **WhatsApp / Tel:** (444) 550 9700
- **Correo:** ige.osvaldocatano@gmail.com
- **Instagram:** [@ige.osvaldocatano](https://instagram.com/ige.osvaldocatano)
