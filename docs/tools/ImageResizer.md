# 📏 Image Resizer — Guía Oficial de Uso

<div align="center">

<img src="../../assets/neko_recizer.svg" alt="NekoTools pensando en dimensionar img" width="140">

**Redimensiona imágenes a resoluciones exactas, porcentajes de escala o presets estándar manteniendo proporciones y fidelidad visual — 100% local en tu navegador.**

[![Client-Side Only](https://img.shields.io/badge/Privacy-100%25_Client--Side-10B981?style=for-the-badge)](https://tools.cinlodev.com)
[![Web Workers](https://img.shields.io/badge/Performance-Web_Workers-6366F1?style=for-the-badge)](https://tools.cinlodev.com)

</div>

---

## ⚡ ¿Qué hace Image Resizer?

**Image Resizer** es una herramienta de ajuste de dimensiones de precisión diseñada para desarrolladores web, diseñadores y creadores digitales. Permite redimensionar archivos de imagen (`PNG`, `JPG`, `WebP`) en milisegundos, ofreciendo control granular sobre el ancho, alto, relación de aspecto, porcentaje de escala y formato de salida.

Todo el procesamiento ocurre localmente dentro de tu navegador web (mediante APIs de Canvas e ImageBitmap), garantizando que tus imágenes **nunca** se suban a ningún servidor externo.

---

## ✨ Características Principales

* **📐 Dimensiones Personalizadas:** Ingresa cualquier valor exacto en píxeles para **Ancho (`Width`)** y **Alto (`Height`)**.
* **🔗 Bloqueo de Relación de Aspecto (Lock Aspect Ratio):** Mantén la proporción original para evitar distorsiones o deformaciones de la imagen al modificar un lado.
* **⚡ Porcentajes Rápidos:** Ajusta instantáneamente la imagen al **25%**, **50%**, **75%** o **100%** de su tamaño original.
* **🎯 Presets de Dimensiones Estándar:** Ajusta con un solo clic a resoluciones habituales:
  * **Full HD (16:9):** `1920 x 1080 px`
  * **HD (16:9):** `1280 x 720 px`
  * **Instagram (1:1):** `1080 x 1080 px`
  * **Standard Web (4:3):** `800 x 600 px`
* **🔄 Conversión de Formato y Calidad:** Exporta manteniendo el formato original o conviértelo en el acto a **WebP**, **PNG** o **JPEG**, con control de calidad de compresión mediante slider interactivo.
* **📊 Comparación en Tiempo Real:** Visualiza las dimensiones y peso en KB/MB antes y después del redimensionado.

---

## 🛠️ Cómo Usar Image Resizer (Paso a Paso)

### 1. Sube tu Imagen
* Arrastra una imagen (`PNG`, `JPG` o `WebP`) a la zona de carga o selecciónala desde tu explorador de archivos.
* Verás de inmediato una vista previa visual con una cuadrícula de transparencia y los datos de la imagen original en el panel de control.

---

### 2. Configura las Nuevas Dimensiones
Tienes 3 formas de ajustar el tamaño de tu imagen:

1. **Ajuste Libre / Manual (Ancho y Alto en píxeles):**
   * Escribe el ancho o alto deseado en las cajas de texto de la derecha.
   * Si el icono del candado está cerrado (acceso **Lock Aspect Ratio** activado en color azul), el otro valor se recalcula automáticamente para conservar la proporción exacta.

2. **Porcentaje de Escala:**
   * Haz clic en **25%**, **50%**, **75%** o **100%** para escalar proporcionalmente la imagen al porcentaje seleccionado. El botón seleccionado quedará iluminado.

3. **Ajustes Rápidos (Quick Presets):**
   * Selecciona uno de los botones predefinidos (`Full HD`, `HD`, `Instagram` o `Standard Web`) para aplicar dimensiones estándar de la industria.

---

### 3. Selecciona el Formato y la Calidad de Salida
* Por defecto se selecciona **Original**, que mantiene el formato del archivo subido.
* Puedes cambiar el formato final seleccionando **WEBP**, **PNG** o **JPEG**.
* Si eliges **WEBP** o **JPEG**, aparecerá un control deslizante (**Calidad de Compresión**) donde podrás calibrar la relación entre nitidez visual y tamaño de archivo (desde modo compacto hasta máxima fidelidad).

---

### 4. Redimensiona y Descarga
* Haz clic en el botón principal **✨ Resize Image / Redimensionar Imagen**.
* Tras el procesamiento instantáneo, el panel inferior te mostrará el peso exacto resultante en verde y aparecerá el botón **Descargar Imagen**.
* Si deseas cargar otra imagen, haz clic en el botón con icono de papelera (**Remove Image / Eliminar Imagen**) en la esquina superior derecha de la tarjeta.

---

## 🔒 Garantía de Privacidad y Rendimiento

Al igual que el resto del ecosistema **NekoTools**, esta herramienta se ejecuta exclusivamente del lado del cliente (`Client-Side First`). Tu imagen se decodifica y renderiza localmente en la memoria de tu dispositivo, garantizando privacidad total y velocidad máxima de ejecución.
