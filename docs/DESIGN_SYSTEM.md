# 🐈 NekoTools - Sistema de Diseño

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

# Sistema de UI

El sistema de interfaz de NekoTools fue diseñado para que todas las herramientas compartan una identidad visual consistente, moderna y altamente reutilizable.

La prioridad no es únicamente la estética, sino también la mantenibilidad. Cualquier nueva herramienta debe poder integrarse utilizando los mismos componentes, layouts y patrones visuales sin necesidad de reinventar la interfaz.

---

# Objetivos

- Mantener una identidad visual consistente.
- Reducir duplicación de código.
- Facilitar la creación de nuevas herramientas.
- Centralizar estilos y variantes.
- Garantizar accesibilidad y responsive design.
- Mantener una experiencia premium en toda la plataforma.

---

# Filosofía

NekoTools utiliza una interfaz inspirada en productos modernos como:

- Linear
- Raycast
- Vercel
- Arc Browser
- Figma

Los principios son:

- mucho espacio en blanco
- interfaces limpias
- jerarquía visual clara
- animaciones sutiles
- bordes suaves
- tipografía protagonista
- colores mínimos

La interfaz nunca debe competir con la herramienta.

La herramienta siempre es el foco.

---

# Design Tokens

Todos los colores, radios, sombras y espaciados provienen del sistema de tokens.

Está prohibido utilizar valores hardcodeados.

Ejemplo:

❌ Incorrecto

```tsx
className="bg-slate-900 rounded-xl p-6"
```

✅ Correcto

```tsx
className="bg-surface-card rounded-card shadow-premium"
```

Si un token no existe, primero debe agregarse al Design System.

Nunca se hardcodea.

---

# Componentes Compartidos

Toda la UI reutilizable vive dentro de:

```
src/shared/ui/
```

Ejemplo:

```
shared/ui/

button/
card/
badge/
input/
tooltip/
modal/
tabs/
stack/
container/
tool-shell/
upload-zone/
result-actions/
loading/
empty-state/
```

Los componentes son completamente independientes de las herramientas.

No conocen lógica de negocio.

Solo reciben props.

---

# Estructura de un componente

Cada componente sigue la misma organización.

```
button/

button.tsx
button.variants.ts
index.ts
```

Donde:

**button.tsx**

Contiene únicamente la estructura del componente.

**button.variants.ts**

Define variantes mediante CVA.

Ejemplo:

- primary
- secondary
- ghost
- destructive

**index.ts**

Exporta la API pública.

---

# Layout Principal

Todas las herramientas utilizan el mismo contenedor.

```
ToolShell
```

Responsabilidades:

- título
- descripción
- acciones
- contenido
- footer
- estado de carga
- cancelación

Cada herramienta simplemente inyecta su contenido.

---

# UploadZone

Todas las herramientas que reciben archivos utilizan el mismo componente.

Funciones:

- drag & drop
- selección manual
- validación
- preview
- estados
- errores

No existen implementaciones duplicadas.

---

# ResultActions

Todas las herramientas muestran sus resultados utilizando el mismo patrón.

Acciones disponibles según la herramienta:

- Copiar
- Descargar
- Compartir
- Limpiar
- Volver a ejecutar

Esto mantiene una experiencia consistente para el usuario.

---

# Animaciones

Las animaciones son discretas.

Nunca deben distraer.

Se utilizan únicamente para mejorar la percepción de fluidez.

Tecnología:

- Framer Motion

Tipos de animaciones:

- Fade
- Slide
- Scale
- Layout Animation

Evitar:

- Bounce
- Elastic
- Animaciones excesivas

---

# Iconografía

Toda la plataforma utiliza:

- Lucide React

No mezclar múltiples librerías de iconos.

Las herramientas mantienen el mismo estilo visual.

---

# Tipografía

Fuente principal:

- Inter

Jerarquía:

- H1
- H2
- H3
- Body
- Caption

La tipografía es uno de los pilares de la identidad visual.

---

# Responsive Design

Toda la plataforma está diseñada mobile-first.

Breakpoints:

- Mobile
- Tablet
- Desktop
- Wide

Los layouts deben adaptarse automáticamente.

Nunca crear versiones independientes.

---

# Accesibilidad

Todas las herramientas deben cumplir:

- navegación mediante teclado
- focus visible
- contraste adecuado
- labels descriptivos
- ARIA cuando corresponda

La accesibilidad forma parte del diseño.

No es un agregado posterior.

---

# Dark First

NekoTools fue diseñado originalmente para modo oscuro.

Todo nuevo componente debe implementarse primero en Dark Mode.

Posteriormente puede extenderse a otros temas.

---

# Branding

La personalidad visual de NekoTools se basa en un equilibrio entre productividad y creatividad.

La mascota **Neko** acompaña la experiencia de forma sutil.

Distribución recomendada:

- 80% interfaz profesional
- 20% identidad de marca

Nunca debe convertirse en un elemento distractor.

---

# Consistencia

Antes de crear un nuevo componente debe verificarse si ya existe uno equivalente dentro de `shared/ui`.

La reutilización siempre tiene prioridad sobre la creación de nuevos componentes.

Una interfaz consistente facilita el aprendizaje del usuario y acelera el desarrollo de nuevas herramientas.

Ese es uno de los principios fundamentales de la plataforma.