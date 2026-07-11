# 🐈 NekoTools - SEO

<div align="center">

<img src="../assets/nekotools.svg" alt="NekoTools Logo" width="140">

<p align="center">
  <strong>Herramientas para desarrolladores y creativos, rápidas, privadas y modernas.</strong>
</p>

<br>

[![Vite](https://img.shields.io/badge/Vite-8.x-646CFF?style=for-the-badge&logo=vite)](https://vite.dev)
[![React](https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org)

</div>

---

## Objetivo

NekoTools está diseñado desde el inicio con una estrategia **SEO-first**, donde cada herramienta funciona como una landing independiente capaz de posicionarse por sí sola en buscadores.

La filosofía del proyecto consiste en construir un ecosistema de utilidades que generen tráfico orgánico continuo mediante búsquedas de alta intención.

---

# Estrategia General

En lugar de tener una única aplicación con diferentes pestañas, cada herramienta posee:

* URL propia
* Metadata propia
* Open Graph específico
* Keywords específicas
* Contenido indexable
* Enlaces internos hacia otras herramientas

Ejemplo:

```
tools.cinlodev.com/webp-converter

tools.cinlodev.com/image-resizer

tools.cinlodev.com/base64

tools.cinlodev.com/svg-to-react

tools.cinlodev.com/palette-extractor

tools.cinlodev.com/remove-bg
```

Cada una funciona como una landing page independiente.

---

# Objetivos SEO

El proyecto busca posicionarse en búsquedas como:

* webp converter
* convert image to webp
* image resizer
* svg to react
* image to base64
* placeholder generator
* color palette extractor
* remove image background
* favicon generator
* markdown preview
* css gradient generator

Estas búsquedas poseen miles de consultas mensuales y una intención muy alta.

---

# Arquitectura de URLs

La estructura del sitio es plana.

```
/

/webp-converter

/image-resizer

/base64

/palette-extractor

/svg-to-react

/remove-bg

/placeholder-generator
```

No existen niveles innecesarios.

Cada herramienta vive en una ruta corta y fácil de recordar.

---

# Metadata

Cada página debe definir:

* title
* description
* canonical
* Open Graph
* Twitter Card
* keywords
* robots

Ejemplo:

```
Title

SVG to React Converter | NekoTools

Description

Convierte archivos SVG en componentes React listos para producción directamente desde tu navegador.

Canonical

https://tools.cinlodev.com/svg-to-react
```

---

# Open Graph

Cada herramienta posee su propia imagen de preview.

Ejemplo:

```
/og/webp-converter.png

/og/svg-to-react.png

/og/image-resizer.png
```

Esto mejora la apariencia al compartir enlaces en:

* LinkedIn
* Discord
* Slack
* Twitter
* Facebook

---

# Sitemap

Todas las herramientas públicas deben aparecer automáticamente en:

```
/sitemap.xml
```

Las rutas internas de desarrollo nunca deben indexarse.

No deben aparecer:

* sesiones
* playgrounds
* páginas experimentales
* demos internas

---

# Robots

El proyecto expone un único archivo:

```
/robots.txt
```

Permitirá indexar todas las herramientas públicas y bloqueará cualquier ruta privada o experimental.

---

# Canonical URLs

Cada página define su URL canónica para evitar contenido duplicado.

Ejemplo:

```
<link rel="canonical" href="https://tools.cinlodev.com/svg-to-react">
```

---

# Enlaces Internos

Todas las herramientas se conectan entre sí.

Ejemplo:

Desde WebP Converter:

* Image Resizer
* Palette Extractor
* Remove Background

Desde SVG to React:

* SVG Cleaner
* Base64
* Placeholder Generator

Esto distribuye autoridad entre páginas y mejora el rastreo de buscadores.

---

# Performance

El rendimiento forma parte de la estrategia SEO.

Objetivos:

* Lighthouse superior a 95
* CLS cercano a 0
* LCP menor a 2 segundos
* JavaScript dividido por rutas
* Lazy Loading de herramientas
* Imágenes optimizadas
* Assets comprimidos

---

# Accesibilidad

Todas las herramientas deben cumplir buenas prácticas de accesibilidad:

* HTML semántico
* Labels correctos
* Navegación por teclado
* Contraste adecuado
* Textos alternativos
* Estados visibles de foco

Además de mejorar la experiencia del usuario, esto aporta señales positivas para los motores de búsqueda.

---

# Contenido

Cada herramienta incluirá una pequeña explicación sobre:

* qué hace
* cuándo utilizarla
* ventajas
* formatos soportados
* preguntas frecuentes

El objetivo es ofrecer contexto suficiente para mejorar el posicionamiento sin convertir la aplicación en un blog.

---

# Estrategia de Crecimiento

Cada nueva herramienta aporta una nueva puerta de entrada al ecosistema.

La prioridad es desarrollar utilidades con:

* alta demanda de búsqueda
* procesamiento local
* buena experiencia de usuario
* reutilización de la infraestructura existente

Con el crecimiento del catálogo, NekoTools se convierte progresivamente en una plataforma de referencia para desarrolladores, diseñadores y creadores de contenido.

---

# Filosofía

El SEO no se considera una etapa final del proyecto.

Forma parte de la arquitectura desde el primer día.

Cada nueva herramienta debe diseñarse pensando en:

* utilidad real
* rendimiento
* privacidad
* experiencia de usuario
* capacidad de posicionamiento orgánico

El objetivo es construir un ecosistema que crezca de forma sostenible mediante contenido útil, herramientas de calidad y una estructura técnica preparada para escalar.
