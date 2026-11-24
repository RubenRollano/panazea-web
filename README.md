# Panazea Software — Web Corporativa

Sitio web corporativo minimalista, de alto rendimiento y diseño premium para **Panazea Software** ([panazea.net](https://panazea.net)).

---

## 🛠️ Stack y Filosofía Técnica

- **HTML5 semántico** estructurado para SEO y accesibilidad.
- **CSS moderno** sin dependencias externas ni frameworks pesados.
- **Zero npm / Zero build step**: Carga instantánea, peso mínimo (< 25 KB total) y máxima puntuación en Google Core Web Vitals / Lighthouse (100/100).
- **Identidad de Marca**: Basada en la Guía de Uso de Marca oficial de PanaZea (fondo blanco y superficies limpias, tipografías Audiowide y Roboto, colores oficiales #4CABD5, #390094 y #E6C20F).


---

## 🚀 Despliegue en Producción (AWS)

El sitio es 100% estático y se sirve desde **AWS**: un bucket privado de S3 (`panazea-web`, `eu-north-1`) detrás de CloudFront (distribución `E321OBTV7EW240`, certificado de ACM). El DNS de `panazea.net` está en **Route 53**. Salió de Cloudflare porque en España los bloqueos por rango de IP en las noches de partido de La Liga afectan a Cloudflare.

- **Despliegue automático:** cada push a `main` ejecuta `.github/workflows/desplegar.yml`, que sincroniza `index.html`, `styles.css`, los favicons y `assets/` con S3 y vacía la caché de CloudFront. No hay paso de compilación. Un fichero nuevo que deba publicarse se añade a las listas `--include` del workflow.
- **Credenciales:** los secretos `AWS_ACCESS_KEY_ID` y `AWS_SECRET_ACCESS_KEY` del repositorio son del usuario `panazea-web-deploy`, que solo puede escribir en ese bucket y crear invalidaciones en esa distribución.
- **`www.panazea.net`** redirige con 301 a `https://panazea.net` mediante la función de CloudFront `panazea-web-peticion`. Una ruta que no existe devuelve `index.html` con 404.
- **Correo:** `panazea.net` usa Google Workspace; sus registros (MX, SPF, DKIM y DMARC) viven en la zona de Route 53 y no deben tocarse al cambiar la web.
- **Registrador:** DonDominio, con los servidores de nombres de Route 53.

---

## 🌐 Ecosistema y Productos Propios

Panazea Software combina la consultoría enterprise de alto nivel con la creación de productos digitales propios bajo una arquitectura SaaS desacoplada:

| Plataforma | Dominio | Infraestructura | Propósito |
| --- | --- | --- | --- |
| **Panazea Software** | `https://panazea.net` | AWS (S3 + CloudFront) | Web corporativa y consultoría de ingeniería |
| **Espigalia (Landing)** | `https://espigalia.com` | AWS (S3 + CloudFront + Lambda) | Web comercial pública del producto flagship |
| **Espigalia (App)** | `https://app.espigalia.com` | Render | Aplicación SaaS (IA, nutrición, Garmin) |

### Enlaces y Relación:
- **En `panazea.net`**: La sección *Producto Propio* presenta a Espigalia y enlaza a `https://espigalia.com`.
- **En `espigalia.com`**: La web tiene entidad propia e independiente, figurando Panazea Software SLU de forma discreta únicamente en el pie de página legal.

---

## 📝 Enlaces y Contacto

- **Correo de contacto**: `ruben.rollano@panazea.net`
- **Perfil de LinkedIn**: [linkedin.com/in/rubenrollano](https://www.linkedin.com/in/rubenrollano)
- **Credencial SAP BTP**: [Verificación en Credly](https://www.credly.com/badges/3380ab03-8b4d-43ec-b5f9-6e237483f044)

