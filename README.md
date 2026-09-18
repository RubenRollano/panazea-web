# Panazea Software SLU — Web Corporativa

Sitio web corporativo minimalista, de alto rendimiento y diseño premium para **Panazea Software SLU** ([panazea.net](https://panazea.net)).

---

## 🛠️ Stack y Filosofía Técnica

- **HTML5 semántico** estructurado para SEO y accesibilidad.
- **CSS moderno** sin dependencias externas ni frameworks pesados.
- **Zero npm / Zero build step**: Carga instantánea, peso mínimo (< 20 KB total) y máxima puntuación en Google Core Web Vitals / Lighthouse (100/100).
- **Estética**: Inspirada en estándares de diseño de *Linear* y *Vercel* (dark mode pulido, tipografía Inter, microdetalles cuidados).

---

## 🚀 Despliegue en Producción (Cloudflare Pages o Vercel)

El sitio es 100% estático, lo que permite alojarlo de forma gratuita con CDN global y certificados SSL automáticos.

### Opción A: Despliegue en Cloudflare Pages (Recomendado)

1. **Subir a GitHub**:
   - Crea un repositorio en tu cuenta de GitHub (ejemplo: `panazea-web`).
   - Sube tu código (ver sección de Git abajo).

2. **Conectar con Cloudflare Pages**:
   - Accede al panel de [Cloudflare Dashboard](https://dash.cloudflare.com/) > **Workers & Pages** > **Create application** > pestaña **Pages** > **Connect to Git**.
   - Selecciona el repositorio `panazea-web`.
   - En **Build settings**:
     - *Framework preset*: `None`
     - *Build command*: (dejar vacío)
     - *Build output directory*: `/` (o déjalo en la raíz)
   - Pulsa **Save and Deploy**.

3. **Asignar el dominio `panazea.net`**:
   - En la página del proyecto en Cloudflare Pages, ve a **Custom domains** > **Set up a custom domain**.
   - Escribe `panazea.net` y `www.panazea.net`.
   - Si tu dominio ya está gestionado en Cloudflare DNS, los registros CNAME se crean automáticamente con un solo clic. Si está en otro registrador, Cloudflare te dará los registros CNAME/DNS a añadir.

---

### Opción B: Despliegue en Vercel

1. **Subir a GitHub** (igual que en la Opción A).
2. **Importar en Vercel**:
   - Entra en [vercel.com](https://vercel.com) > **Add New Project** > Importar `panazea-web`.
   - Framework Preset: **Other**.
   - Pulsa **Deploy**.
3. **Asignar el dominio `panazea.net`**:
   - Ve a **Project Settings** > **Domains**.
   - Añade `panazea.net` y `www.panazea.net`.
   - Vercel te indicará el registro `A` (`76.76.21.21`) o `CNAME` (`cname.vercel-dns.com`) para tu DNS.

---

## 📝 Personalizaciones Pendientes

- **NIF/CIF**: En el pie de página de `index.html` (`línea 204`), sustituye `B-XXXXXXXX` por el CIF definitivo de Panazea Software SLU.
- **Perfil de LinkedIn**: En la sección de perfil de `index.html` (`línea 177`), confirma o ajusta la URL de tu perfil de LinkedIn.
