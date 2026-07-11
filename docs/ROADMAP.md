# 🐈 NekoTools - Ruta de Desarrollo

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

---

# 🗺️ Roadmap

Este documento define la evolución planificada de NekoTools.

Las herramientas se organizan por etapas de desarrollo, priorizando el impacto para el usuario, la reutilización de la infraestructura existente y el crecimiento sostenible de la plataforma.

---

# Estado General

| Categoría | Estado |
|-----------|:------:|
| Infraestructura | ✅ Estable |
| Design System | ✅ Estable |
| Arquitectura Modular | ✅ Estable |
| Herramientas Base | 🚧 En expansión |
| IA Local | 🚧 Planificada |

---

# Fase 1 · Herramientas Fundamentales

Estas herramientas conforman la base del ecosistema.

| Herramienta | Estado |
|-------------|:------:|
| 🖼️ WebP Converter | ✅ |
| 🎨 Palette Extractor | ✅ |
| 📏 Image Resizer | ✅ |
| 🔗 Image to Base64 | ✅ |
| 📐 SVG to React | ✅ |

## Objetivos

- Validar la arquitectura.
- Compartir componentes reutilizables.
- Consolidar el Design System.
- Establecer la experiencia de usuario.
- Construir una base sólida para futuras herramientas.

---

# Fase 2 · Productividad

Enfocada en aumentar la productividad de desarrolladores y diseñadores.

## Herramientas

- 🧩 Placeholder Generator
- ✂️ Background Remover (IA Local)
- 🧹 SVG Cleaner
- 🎭 Favicon Generator
- 🖼️ Open Graph Generator

## Objetivos

- Incorporar procesamiento avanzado.
- Reutilizar la infraestructura existente.
- Expandir las capacidades para diseño y branding.

---

# Fase 3 · Developer Toolkit

Colección de utilidades para el desarrollo diario.

## Formato de datos

- JSON Formatter
- JSON Validator
- Base64 Decoder
- URL Encoder / Decoder

---

## Desarrollo Web

- JWT Decoder
- Regex Tester
- Markdown Preview
- HTML Preview
- CSS Formatter
- CSS Minifier
- JavaScript Beautifier

---

## CSS & UI

- CSS Gradient Generator
- Box Shadow Generator
- Border Radius Generator
- Clamp Generator
- Flex Playground
- Grid Playground

---

## 🖋️ Raster to SVG Converter

Convierte imágenes rasterizadas en archivos SVG editables compatibles con herramientas profesionales de diseño.

### Funcionalidades

- Conversión PNG/JPG/WEBP a SVG.
- Generación de paths vectoriales.
- Detección de colores.
- Eliminación de fondo.
- Simplificación de vectores.
- Exportación SVG optimizado.

### Objetivo

Crear una herramienta rápida para transformar logos e iconos en vectores editables para utilizar en Figma, Affinity Designer e Illustrator.

### Principios

- Procesamiento local.
- Sin subida de archivos.
- Privacidad por defecto.

---

## Tailwind CSS

- Tailwind Class Formatter
- Tailwind Merge Preview
- Tailwind Cheat Sheet
- Color Palette Generator

---

# Fase 4 · Assets

Herramientas para generar recursos gráficos.

- App Icon Generator
- Splash Screen Generator
- Social Image Generator
- SVG Optimizer
- SVG Sprite Generator
- Logo Exporter

## 🎨 Icon Generator / Logo Exporter

Herramienta para transformar un logo o imagen de marca en todos los formatos necesarios para aplicaciones web, móviles y productos digitales.

El objetivo es simplificar la preparación de assets de branding, evitando tener que generar manualmente cada tamaño y formato.

### Funcionalidades

- Subida de logo en SVG o imagen.
- Generación automática de múltiples tamaños.
- Exportación de favicon.
- Generación de iconos PWA.
- Creación de Apple Touch Icon.
- Generación de Open Graph Image.
- Exportación en paquete ZIP.

### Formatos generados
- 16x16, 32x32, 48x48, 64x64, 128x128, 256x256, 512x512, 1024x1024.
- Iconos PWA.
- Apple Touch Icon.
- Open Graph Image.

### Exportación

Exportar todos los iconos como archivos individuales o en un ZIP.

### Opciones avanzadas

- Fondo transparente o personalizado.
- Color de fondo.
- Padding automático.
- Ajuste de escala.
- Safe area para iconos móviles.
- Preview de resultados.

### Integraciones futuras

Puede generar automáticamente:

- `manifest.json`
- etiquetas HTML para favicon.
- estructura de assets recomendada para proyectos web.

### Principios

Como toda herramienta de NekoTools:

- Procesamiento local en navegador.
- Sin subida de archivos.
- Privacidad por defecto.
- Exportación rápida.

---

# Fase 5 · Inteligencia Artificial

Herramientas impulsadas por modelos ejecutados directamente en el navegador.

## Objetivos

- Mantener la privacidad del usuario.
- Evitar dependencias de servicios externos.
- Aprovechar WebGPU y WebAssembly cuando estén disponibles.

## Herramientas

- Remove Background
- Image Upscaler
- OCR Local
- Image Caption Generator
- Colorizer
- Smart Crop

---

# Ideas Futuras

Estas herramientas forman parte del backlog y podrán incorporarse según la evolución del proyecto.

---

## Desarrollo

- Git Ignore Generator
- Docker Compose Generator
- Dockerfile Generator
- REST Client
- Cron Expression Builder

---

## Productividad

- UUID Generator
- Nano ID Generator
- Password Generator
- Hash Generator
- QR Generator

---

## Texto

- Lorem Ipsum
- Case Converter
- Slug Generator
- Word Counter
- Markdown Editor

---

## Colores

- Contrast Checker
- Accessibility Analyzer
- Theme Generator
- OKLCH Playground

---

# Principios para nuevas herramientas

Antes de incorporar una nueva utilidad debe cumplir, al menos, con estos criterios:

- Resolver un problema real.
- Ser útil de forma recurrente.
- Mantener la filosofía Privacy First.
- Compartir la arquitectura existente.
- Aprovechar el Design System.
- No duplicar funcionalidades ya presentes.

---

# Visión

El objetivo no es crear cientos de herramientas.

El objetivo es construir una colección cuidadosamente seleccionada de utilidades que destaquen por su calidad, velocidad, consistencia y experiencia de uso.

Cada nueva herramienta debe sentirse como una extensión natural de NekoTools y fortalecer el ecosistema completo.