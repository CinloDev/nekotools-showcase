# 📐 SVG to React Code — Guía Oficial de Uso

<div align="center">

<img src="../../assets/neko_svg_react.svg" alt="NekoTools pensando en convertor img" width="140">

**Limpia, optimiza y convierte gráficos vectoriales SVG en componentes JSX / TSX listos para React — 100% local en tu navegador.**

[![Client-Side Only](https://img.shields.io/badge/Privacy-100%25_Client--Side-10B981?style=for-the-badge)](https://tools.cinlodev.com)
[![TypeScript Ready](https://img.shields.io/badge/Stack-TypeScript_%2F_JSX-6366F1?style=for-the-badge)](https://tools.cinlodev.com)

</div>

---

## ⚡ ¿Qué hace SVG to React Code?

**SVG to React Code** toma archivos o código SVG crudo exportado desde herramientas de diseño (Figma, Illustrator, Inkscape) y los transforma automáticamente en **componentes funcionales de React limpios, optimizados y altamente reutilizables**.

Resuelve de manera automática los problemas más habituales al pegar un SVG en React:
- Conversión instantánea de atributos `kebab-case` de HTML/XML a `camelCase` de JSX (`stroke-width` → `strokeWidth`, `fill-rule` → `fillRule`, `clip-path` → `clipPath`).
- Eliminación de metadatos pesados, etiquetas innecesarias (`<defs>`, comentarios, identificadores de editor) e inline-styles.
- Tipado estricto opcional para TypeScript (`SVGProps<SVGSVGElement>`).
- Normalización de colores hacia `currentColor` para un control total con clases CSS o Tailwind CSS.

---

## ✨ Características Principales

* **⚛️ Conversión Dual (`JSX` o `TSX`):**
  * **JSX Estándar:** Componente funcional rápido para proyectos JavaScript.
  * **Soporte TypeScript (`TSX`):** Genera código tipado extendiendo `React.SVGProps<SVGSVGElement>` para autocompletado perfecto de props (`className`, `onClick`, `style`, etc.).
* **🎨 Opción `currentColor` Inteligente:**
  * Al activar **Usar currentColor**, reemplaza automáticamente los colores estáticos del atributo `fill` o `stroke` para que el icono herede la clase de color de su contenedor (`text-indigo-500`, `text-emerald-400`, etc.).
* **📐 Limpieza Dinámica de Dimensiones (`Clean Dimensions`):**
  * Elimina atributos fijos `width` y `height` preservando el `viewBox`, permitiendo redimensionar el icono libremente con clases CSS (`w-6 h-6`).
* **👁️ Previsualización en Vivo & Código SVG Limpio:**
  * Pestañas duales en el panel de código para copiar el **Componente React** o el **Código SVG Limpio y Optimizado**.

---

## 🛠️ Cómo Usar SVG to React Code (Paso a Paso)

### 1. Sube tu Archivo SVG
* Arrastra tu archivo `.svg` a la zona de subida o selecciónalo de tu explorador de archivos.

---

### 2. Configura tu Componente
En el panel lateral izquierdo (**Ajustes del Conversor**):
1. **Nombre del Componente:** Escribe el nombre PascalCase para tu componente (por ejemplo: `LogoIcon`, `UserAvatarSvg`).
2. **Soporte TypeScript:** Actívalo si trabajas en un proyecto `.tsx`.
3. **Usar currentColor:** Actívalo si quieres pintar el icono dinámicamente con CSS o Tailwind.
4. **Limpiar Dimensiones:** Actívalo para que el componente sea 100% responsivo.

---

### 3. Previsualiza y Copia el Código
* Observa el renderizado en vivo y haz clic en **Copiar Código** para copiar tu componente React listo para pegar en tu proyecto.

---

## 🔒 Privacidad y Arquitectura Client-Side

1. **100% Local en tu Navegador:** Tus archivos e ilustraciones vectoriales se procesan en la memoria local y nunca se transmiten a servidores externos.
