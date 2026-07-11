# 🐈 NekoTools - Arquitectura

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

## Filosofía

NekoTools está construido como una plataforma de herramientas para desarrolladores y creadores de contenido.

Cada herramienta debe poder evolucionar de forma independiente, compartir componentes con el resto del ecosistema y mantener una experiencia consistente para el usuario.

La arquitectura prioriza:

- Escalabilidad.
- Reutilización de código.
- Alto rendimiento.
- Procesamiento local (Client-Side First).
- Bajo costo de infraestructura.
- SEO para cada herramienta.

---

# Estructura General

```text
src/
│
├── app/                # Configuración principal
├── pages/              # Páginas y rutas
├── shared/             # Componentes reutilizables
│
├── features/
│   ├── webp-converter/
│   ├── image-resizer/
│   ├── palette-extractor/
│   ├── image-to-base64/
│   ├── svg-to-react/
│   ├── placeholder-generator/
│   └── remove-background/
│
├── assets/
├── styles/
└── utils/
```

Cada herramienta vive dentro de su propia Feature.

No existen dependencias directas entre Features.

Todo el código compartido vive dentro de `shared`.

---

# Arquitectura por Features

Cada herramienta sigue exactamente la misma estructura.

```text
feature/

ui/
hooks/
services/
workers/
types/
config/
constants/
utils/
index.ts
```

No todas las carpetas son obligatorias.

Solo se crean cuando la herramienta realmente las necesita.

---

# Capas

La aplicación está dividida en capas claramente definidas.

## UI

Responsable únicamente del renderizado.

No contiene lógica de negocio.

---

## Hooks

Gestionan el estado.

Coordinan la UI.

Invocan servicios.

---

## Services

Contienen la lógica de procesamiento.

Pueden comunicarse con:

- Web Workers
- APIs
- Librerías externas

---

## Workers

Se utilizan únicamente cuando una operación puede bloquear el hilo principal.

Ejemplos:

- procesamiento de imágenes
- IA local
- compresión
- análisis de SVG

---

## Shared

Todo componente reutilizable pertenece aquí.

Ejemplos:

- Buttons
- Cards
- Inputs
- Dialogs
- ToolShell
- UploadZone
- Progress
- ResultActions

---

# Client-Side First

La mayor parte del procesamiento ocurre directamente en el navegador.

Beneficios:

- privacidad total
- menor costo operativo
- mejor velocidad
- funcionamiento offline parcial
- menor latencia

El servidor únicamente aloja la aplicación.

---

# Diseño Modular

Cada herramienta debe poder:

- desarrollarse de forma independiente
- reutilizar componentes existentes
- compartir el mismo sistema visual
- compartir la navegación
- compartir el sistema de temas

---

# Escalabilidad

La arquitectura está preparada para incorporar decenas de herramientas sin modificar la estructura principal.

Ejemplo:

```text
features/

webp-converter
palette-extractor
image-resizer
image-to-base64
svg-to-react
placeholder-generator
remove-background
favicon-generator
json-formatter
jwt-decoder
regex-tester
markdown-preview
...
```

Cada nueva herramienta simplemente agrega una nueva Feature.

---

# Rendimiento

Se priorizan las siguientes prácticas:

- Lazy Loading de herramientas.
- Code Splitting.
- Web Workers cuando sea necesario.
- Procesamiento local.
- Componentes reutilizables.
- Evitar renders innecesarios.
- Optimización de imágenes.

---

# SEO

Cada herramienta posee su propia ruta.

Ejemplo:

```text
/webp-converter

/image-resizer

/base64

/svg-to-react

/palette-extractor
```

Esto permite posicionar cada utilidad individualmente en buscadores.

---

# Objetivo

NekoTools no es una aplicación con múltiples funciones.

Es una plataforma de herramientas independientes que comparten una misma experiencia de usuario, un mismo lenguaje visual y una arquitectura común.