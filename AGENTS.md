# Panazea Software — Reglas del Proyecto y Agentes

Este repositorio contiene el sitio web corporativo de **Panazea Software** ([panazea.net](https://panazea.net)), boutique de ingeniería de software, arquitectura cloud y consultoría tecnológica especializada, liderada por Rubén Rollano.

---

## Identidad y Posicionamiento

Panazea Software combina más de 20 años de experiencia en arquitectura tecnológica de misión crítica con el desarrollo de productos digitales propios:
- **Especialización Enterprise**: Consultoría y arquitectura sobre SAP BTP (Business Technology Platform), Clean Core, CAP (Cloud Application Programming), ABAP RAP y arquitecturas *event-driven*.
- **Desarrollo de Producto Propio**: Creadores y desarrolladores de **Espigalia** ([espigalia.com](https://espigalia.com)), producto insignia de salud y nutrición inteligente.

---

## Principios Técnicos y de Rendimiento

1. **Zero npm / Zero build step**:
   - Todo el sitio se implementa en **HTML5 semántico puro** (`index.html`) y **CSS vanilla moderno** (`styles.css`).
   - Cero dependencias en `package.json`. No introducir compiladores, bundlers ni dependencias de npm sin aprobación explícita.
   - Rendimiento objetivo: Core Web Vitals y Lighthouse **100/100**. Carga < 20 ms desde CDN.
2. **Sistema Visual**:
   - Tipografía: **Audiowide** para marca e identidad, **Roboto** para lectura.
   - Colores oficiales: `#4CABD5` (azul cian), `#390094` (morado profundo), `#E6C20F` (oro/ámbar).
   - Fondos limpios y superficies claras con sutiles toques de resplandor ambiental.

---

## Ecosistema de Dominios y Despliegue

| Entidad | Dominio | Alojamiento | Repositorio |
| --- | --- | --- | --- |
| **Panazea Software (Web Corporativa)** | `https://panazea.net`<br>`https://www.panazea.net` | Cloudflare Pages | `RubenRollano/panazea-web` (rama `main`) |
| **Espigalia (Web Pública / Landing)** | `https://espigalia.com`<br>`https://www.espigalia.com` | Cloudflare Pages | `RubenRollano/Espigalia` (`apps/landing`) |
| **Espigalia (Aplicación SaaS)** | `https://app.espigalia.com` | Render | `RubenRollano/Espigalia` (raíz Next.js) |

---

## Especialistas del Proyecto

- `panazea-brand` (`agents/panazea-brand.md`): Guardián de la marca, fidelidad de la identidad visual, métricas Lighthouse y presentación adecuada de los productos propios.
