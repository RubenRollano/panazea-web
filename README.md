# Panazea Software — Web Corporativa

Sitio web corporativo minimalista, de alto rendimiento y diseño premium para **Panazea Software** ([panazea.net](https://panazea.net)).

---

## 🛠️ Stack y Filosofía Técnica

- **HTML5 semántico** estructurado para SEO y accesibilidad.
- **CSS moderno** sin dependencias externas ni frameworks pesados.
- **Zero npm / Zero build step**: Carga instantánea, peso mínimo (< 25 KB total) y máxima puntuación en Google Core Web Vitals / Lighthouse (100/100).
- **Identidad de Marca**: Basada en la Guía de Uso de Marca oficial de PanaZea (fondo blanco y superficies limpias, tipografías Audiowide y Roboto, colores oficiales #4CABD5, #390094 y #E6C20F).


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

## 📝 Enlaces y Contacto

- **Correo de contacto**: `ruben.rollano@panazea.net`
- **Perfil de LinkedIn**: [linkedin.com/in/rubenrollano](https://www.linkedin.com/in/rubenrollano)
- **Credencial SAP BTP**: [Verificación en Credly](https://www.credly.com/badges/3380ab03-8b4d-43ec-b5f9-6e237483f044)

