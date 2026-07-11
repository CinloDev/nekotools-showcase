# 🐈 NekoTools - Guia de Contribución

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

## Introducción

Explicar que NekoTools busca mantener una plataforma consistente y escalable.

Ejemplo:

NekoTools está construido bajo una arquitectura modular donde cada herramienta funciona como una Feature independiente, compartiendo infraestructura común.

Cualquier contribución debe respetar los principios de privacidad, rendimiento, diseño y calidad definidos por el proyecto.

---

# Antes de contribuir

Antes de crear una nueva herramienta o modificar una existente:

- Revisar la arquitectura.
- Revisar el Design System.
- Buscar componentes existentes.
- Evitar duplicación de lógica.
- Mantener la filosofía Client-Side First.

---

# Arquitectura de Features

Cada herramienta debe vivir dentro de:

src/features/

Ejemplo:

features/
└── image-resizer/
    ├── ui/
    ├── hooks/
    ├── services/
    ├── workers/
    ├── types/
    ├── constants/
    └── index.ts

---

# Reglas de desarrollo

## Separación de responsabilidades

### UI

Debe encargarse únicamente de:

- Renderizado.
- Estados visuales.
- Interacción del usuario.

No debe contener lógica de procesamiento.

---

### Services

Contienen:

- procesamiento de archivos.
- comunicación con APIs.
- transformaciones.
- operaciones complejas.

---

### Hooks

Gestionan:

- estado.
- ciclo de vida.
- coordinación entre UI y servicios.

---

### Workers

Utilizar cuando una operación pueda bloquear el navegador.

Ejemplos:

- procesamiento de imágenes.
- compresión.
- IA local.
- análisis pesado.

---

# Design System

Toda interfaz nueva debe utilizar componentes existentes.

Antes de crear un componente:

1. Buscar si ya existe.
2. Extenderlo si es necesario.
3. Crear uno nuevo solamente cuando sea realmente reutilizable.

No utilizar:

- colores hardcodeados.
- valores arbitrarios.
- estilos duplicados.

---

# Nuevas herramientas

Una nueva herramienta debe cumplir:

## Producto

- Resolver un problema real.
- Tener un caso de uso claro.
- Aportar valor al ecosistema.

## Técnica

- Mantener arquitectura Feature-based.
- Usar infraestructura existente.
- Priorizar procesamiento local.

## Experiencia

- Utilizar ToolShell.
- Mantener UX consistente.
- Funcionar correctamente en mobile.

---

# Privacidad

La privacidad es una regla fundamental.

Siempre priorizar:

1. Procesamiento en navegador.
2. Web APIs.
3. WebAssembly.
4. Web Workers.
5. Modelos locales.

Evitar enviar archivos o datos externos salvo que sea estrictamente necesario.

---

# Rendimiento

Toda contribución debe considerar:

- tamaño del bundle.
- carga inicial.
- memoria utilizada.
- procesamiento eficiente.
- lazy loading.

---

# Código

Convenciones:

- TypeScript estricto.
- Componentes pequeños.
- Nombres descriptivos.
- Evitar duplicación.
- Mantener funciones simples.

---

# Commits

Formato recomendado:

type(scope): description


Ejemplos:

feat(image-resizer): agregar optimización progresiva

test(tools): cubrir casos edge en palette-extractor

fix(ui): corregir renderizado en mobile

chore(deps): actualizar webp-encoder

style(code): aplicar formateo ESLint

perf(worker): optimizar compresión JPEG

docs(contributing): actualizar guidelines


Tipos:

- feat
- fix
- refactor
- docs
- style
- perf
- chore

---

# Pull Requests

Un PR debe incluir:

- descripción del cambio.
- motivo de la modificación.
- capturas si afecta UI.
- pruebas realizadas.

Antes de abrir un PR verificar:

- build correcto.
- lint correcto.
- responsive funcionando.
- dark mode funcionando.

---

# Filosofía

Cada contribución debe mejorar NekoTools sin romper su identidad.

La prioridad siempre será:

1. Calidad.
2. Consistencia.
3. Privacidad.
4. Experiencia del usuario.
5. Velocidad.

NekoTools crece agregando herramientas excelentes, no acumulando funcionalidades.