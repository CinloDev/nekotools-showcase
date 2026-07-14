# 🌟 Favicon & PWA Generator — Guía Oficial de Uso y Arquitectura

<div align="center">

<img src="../../assets/neko_favicon.svg" alt="NekoTools pensando en convertor img" width="140">

**Genera paquetes completos de iconos para web, Progressive Web Apps (PWA), Apple iOS, Android y Windows con previsualización multi-dispositivo — 100% local en tu navegador.**

[![Client-Side Only](https://img.shields.io/badge/Privacy-100%25_Client--Side-10B981?style=for-the-badge)](https://tools.cinlodev.com/favicon-generator)
[![Engine](https://img.shields.io/badge/Engine-JSZip_%2B_Native_ICO-6366F1?style=for-the-badge)](https://tools.cinlodev.com/favicon-generator)

</div>

---

## ⚡ ¿Qué hace Favicon & PWA Generator?

**Favicon & PWA Generator** es un generador profesional todo-en-uno que convierte cualquier imagen o logotipo (`PNG`, `SVG`, `WebP`, `JPG`) en un paquete estandarizado listo para producción en páginas web, Progressive Web Apps y plataformas móviles.

A diferencia de convertidores en línea tradicionales que suben tus activos a servidores externos, **Favicon Generator** ejecuta su motor de renderizado multi-resolución en `HTML5 Canvas`, codificación nativa de archivos `.ico` (`ICO Encoder`) y empaquetado comprimido `JSZip` **100% del lado del cliente**.

---

## ✨ Características Principales

* **🖥️ Inspector Visual Multi-Dispositivo Interactivo (Columna Izquierda):**
  * **Pestaña de Navegador (`Browser Tab`):** Simulación realista de pestaña de navegador moderna en modo oscuro con título configurable, icono de 32px y barra de direcciones URL.
  * **Pantalla iOS (`iPhone iOS`):** Simulación de pantalla de inicio de iPhone con icono estilo Apple Touch (`180×180px`) y bordes redondeados nativos de Apple.
  * **Android PWA (`Android PWA`):** Simulación de icono de cajón de aplicaciones en Android (`192×192px`).
  * **Windows Tile (`Windows Tile`):** Simulación de mosaico del menú Inicio de Windows (`150×150px`).
  * **Grilla de Tamaños (`Todos los Tamaños`):** Inspección visual simultánea de las resoluciones generadas (`16px`, `32px`, `48px`, `150px`, `180px`, `192px`, `512px`).

* **🎨 Edición Estilo Canva (Columna Derecha):**
  * **Modos de Ajuste:** `Contain` (ajustar preservando proporción), `Cover` (llenar lienzo), `Stretch` (estirar a medida).
  * **Control de Zoom & Posición:** Deslizador de zoom (`100% - 300%`) y coordenadas X/Y precisas para centrar logotipos asimétricos.
  * **Fondos y Esquinas:** Soporte para fondos transparentes, sólidos, gradientes lineales o radiales, y bordes con radio seleccionable (`0px`, `8px`, `16px`, `24px`, `Círculo`).

* **📦 Paquete Completo `favicon-package.zip` & Archivos Estandarizados:**
  * **`favicon.ico`** multi-resolución (`16x16`, `32x32`, `48x48`) generado nativamente sin bibliotecas externas.
  * **`favicon.svg`** preservando la ilustración vectorial de origen.
  * **Iconos PNG estandarizados:** `favicon-16x16.png`, `favicon-32x32.png`, `favicon-48x48.png`, `apple-touch-icon.png` (180x180), `android-chrome-192x192.png`, `android-chrome-512x512.png`, `mstile-150x150.png`.
  * **`site.webmanifest`** autogenerado con nombre de PWA, nombre corto, color de tema y color de fondo.
  * **`browserconfig.xml`** para compatibilidad con mosaicos de Windows.
  * **`favicon.html`** con el fragmento exacto de etiquetas `<link>` y `<meta>`.

* **📋 Copia Instantánea de Etiquetas HTML (`<head>`):**
  * Bloque de código interactivo con botón **`Copiar Código HTML`** para pegar al instante en `index.html`.

---

## 🏛️ Arquitectura del Módulo (`src/features/favicon-generator/`)

```text
src/features/favicon-generator/
├── ui/
│   ├── FaviconPreviewTabs.tsx       # Inspector multi-dispositivo y pestañas de simulación
│   ├── FaviconUploadCard.tsx        # Zona de subida Drag & Drop
│   ├── TransformCard.tsx            # Modo de ajuste, Zoom y Desplazamiento X/Y
│   ├── FaviconBackgroundCard.tsx    # Selector de fondo transparente/color/gradiente y radio
│   ├── PwaOptionsCard.tsx           # Configuración de manifiesto PWA y checkboxes
│   ├── FaviconExportCard.tsx        # Botón de descarga de ZIP y copiador de snippet HTML
│   └── favicon-generator-feature.tsx # Orquestador de 2 columnas responsive
├── hooks/
│   └── useFaviconGenerator.ts       # Orquestador del estado y renderizado canvas multi-resolución
├── services/
│   ├── ico-encoder.ts               # Codificador binario client-side para archivos .ico estándar
│   ├── favicon-packager.ts          # Constructor del archivo ZIP comprimido con JSZip
│   └── html-generator.ts            # Generador dinámico de manifiestos y etiquetas HTML
└── types/
    └── favicon.types.ts             # Definiciones estrictas de TypeScript
```
