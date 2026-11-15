# Auditoria y Uso de la IA

## Tabla 1. Auditoria y Uso de la IA - Fase 1 (Mini Avance 1)

| Sección | Integrante(s) | Herramienta y Link al prompt utilizado | Aporte de la IA | Aporte Intelectual del equipo |
| :--- | :--- | :--- | :--- | :--- |
| Repositorio, Despliegue y Descripción del Proyecto | Gonzalez, Walter | Antigravity / Gemini — [Ver prompts en prompts.md](./prompts.md) | Asistió en la estructuración del README en formato Markdown y corrección de coherencia en la redacción inicial. | Configuración del repositorio en GitHub, despliegue en GitHub Pages, y formulación del problema, propósito, objetivo general y alcance del sistema. |
| Identificación de Usuarios | Sanchez, Jose | Ninguna | Ninguno | Análisis y caracterización de los perfiles de Cliente y Administrador, identificando sus necesidades y funciones clave en el sistema. |
| Requisitos Funcionales | Rozette, Jose | Ninguna | Ninguno | Definición técnica y tabulación completa de los requisitos funcionales del sistema (RF-01 a RF-09). |
| Requisitos No Funcionales y Escenarios de Uso | Meneses, Alexander | Ninguna | Ninguno | Formulación de los requisitos no funcionales (RNF-01 a RNF-08) y desarrollo estructurado de los escenarios de uso paso a paso. |

---

## Tabla 2. Auditoria y Uso de la IA - Fase 1 (Parte 2)

| Sección | Integrante(s) | Herramienta y Link al prompt utilizado | Aporte de la IA | Aporte Intelectual del equipo |
| :--- | :--- | :--- | :--- | :--- |
| Casos de Uso, Modelo de Clases, Navegación y Trazabilidad | Gonzalez, Walter | Antigravity / Gemini — [Ver prompts en prompts.md](./prompts.md) | Asistió en la estructuración técnica del README y en la revisión de coherencia de los modelos. | Diseño de casos de uso (flujo principal y excepciones), modelado de clases del dominio, arquitectura de navegación y matriz de trazabilidad. |
| Revisión de Ortografía y Redacción | Sanchez, Jose | Ninguna | Ninguno | Revisión de ortografía, estilo y redacción técnica de los entregables de la parte 2. |
| Validación de Requisitos | Rozette, Jose | Ninguna | Ninguno | Verificación cruzada para asegurar la cobertura de todos los requisitos funcionales en las clases y casos de uso. |
| Control de Estructura | Meneses, Alexander | Ninguna | Ninguno | Inspección de la estructura documental conforme a los criterios de evaluación de la cátedra. |

---

## Tabla 3. Auditoría y Uso de la IA - Fase 2


| Sección | Integrante(s) | Herramienta | Aporte de la IA | Aporte Intelectual del equipo |
| :--- | :--- | :--- | :--- | :--- |
| **Arquitectura de Información y Reglas de Negocio** | Gonzalez, Walter | Antigravity / Gemini — [Ver prompts](./prompts.md) | Maquetación en Markdown, sintaxis Mermaid y revisión de coherencia. | Definición de la arquitectura de información, sitemap y reglas clave: taxonomía deportiva, caducidad TTL (45 min), compuerta de cancelación (> 2h), abono del 30 % y control de canchas sin CRUD. (Terminado). |
| **Modelo y Flujos de Navegación** | Sanchez, Jose | Gemini — [Ver prompts](./prompts.md) | Apoyo en la estructuración y depuración de flujos. | Modelado formal de los 6 flujos críticos, matriz de acceso por roles y auditoría cruzada de consistencia lógica con las pantallas. (Terminado). |
| **Wireframes (Media Fidelidad)** | Rozette, Jose | Figma / Draw.io — Ninguna | Ninguno | Diseño estructural de las 6 pantallas principales en escala de grises para escritorio y móvil responsivo. (Terminado). |
| **Prototipo de Alta Fidelidad** | Meneses, Alexander | Figma — Ninguna | Ninguno | Creación del sistema de diseño accesible (WCAG 2.1 AA) y prototipo navegable interactivo en Figma con enlace público. (Terminado). |


---

## Tabla 4. Auditoría y Uso de la IA - Fase 3 (Implementación Web HTML5 / CSS3)

| Sección / Componente | Integrante(s) | Herramienta y Link al prompt | Aporte de la IA | Aporte Intelectual del equipo |
| :--- | :--- | :--- | :--- | :--- |
| **Arquitectura Global de Estilos, Multimedia y Diseño Visual** | Gonzalez, Walter (25%) | Antigravity / Gemini — [Ver prompts 14, 16 y 17 en prompts.md](./prompts.md) | Recomendó fuentes y plataformas de inspiración visual para botones y componentes modernos (como Uiverse.io), propuso una arquitectura y división de archivos CSS modular (`estilos.css`, `componentes.css` y `responsive.css`) superando la estructura monolítica previa, y asistió en la calibración matemática de variables para sombras verdes multicapa (`--sombra-verde`, `--sombra-verde-hover`) y curvas Bézier de transición. | **Liderazgo integral del 100% del diseño y arquitectura CSS del proyecto:** Creación de las tres hojas de estilo (`estilos.css`, `componentes.css`, `responsive.css`), normalización de tipografías, sistema de diseño responsivo y contraste accesible WCAG 2.1 AA. **Selección, curaduría, edición y optimización del 100% de los recursos multimedia:** Búsqueda y preparación de las imágenes de alta definición de las 15 canchas deportivas en la Provincia de Panamá y recopilación, ajuste y estandarización del set completo de iconos vectoriales SVG oficiales (deportes, superficies, comodidades, estados y navegación), garantizando cero uso de emojis en toda la plataforma. |
| **Maquetación Semántica de Vistas Públicas y Catálogo** | Sanchez, Jose (25%) | Gemini — [Ver prompt 15 en prompts.md](./prompts.md) | Asistió en la depuración y unificación de elementos `<div>` que se encontraban fragmentados y dispersos en la estructura del catálogo, sugiriendo su sustitución por etiquetas de bloque semántico HTML5 estándar. | Maquetación HTML5 semántica y estructuración de la página de inicio (`index.html`) con el hero banner y el collage interactivo de 6 disciplinas deportivas con balones resaltados; maquetación del catálogo general (`catalogo.html`) con las 15 canchas deportivas precargadas y sidebar de filtros facetados por checkboxes y barra de ordenamiento; y estructuración de la página de normativas técnicas y calzado reglamentario (`normas.html`). |
| **Maquetación Semántica de Vistas Transaccionales del Cliente** | Rozette, Jose (25%) | Gemini — [Ver prompts 14 y 15 en prompts.md](./prompts.md) | Asistió en la corrección de enlaces y modales de confirmación e instrucciones de abono que presentaban fallas de apertura al remover JavaScript, recomendando el uso de la pseudo-clase `:target`, y en la unificación de estructuras `<div>` anidadas en las tarjetas de turnos. | Maquetación HTML5 semántica de la ficha técnica de cancha (`detalle.html`), implementando la galería de imágenes, características técnicas y la matriz semanal de disponibilidad horaria con leyenda multimodal accesible; estructuración del panel del cliente "Mis Reservas" (`reservas.html`) con tarjetas de turnos, desglose económico de 4 valores (tarifa, abono 30%, saldo en caja 70% y comprobante ID), filtros de estado y botón Salir; y maquetación de la página de contacto y soporte (`contacto.html`) con canales oficiales de Yappy y WhatsApp (6351-6012). |
| **Maquetación Semántica de Autenticación y Panel Administrativo** | Meneses, Alexander (25%) | Gemini — [Ver prompt 14 en prompts.md](./prompts.md) | Asistió en la corrección de botones de acción y estado (incluyendo el botón "Salir", enlaces de inhabilitación horaria y modales administrativos `:target`), además de la unificación de contenedores repetitivos en las tablas del panel administrativo. | Maquetación HTML5 semántica del módulo unificado de acceso y registro (`login.html`), implementando la alternancia interactiva entre pestañas de Iniciar Sesión y Registrarse mediante radio buttons y etiquetas vinculadas en CSS puro (sin casillas redundantes de "Recordarme"); maquetación del panel integral de control y recepción (`admin.html`), integrando métricas en tarjetas, tabla 8.1 de Gestión de Canchas Precargadas con switch de activación y tabla 8.2 de Reservas con validación de abonos y cobro en sitio POS. |

---

### Resumen de Distribución de Responsabilidades - Fase 3

Para la Fase 3, el equipo dividió el esfuerzo de forma **estrictamente equitativa (25% cada integrante)** en cuanto a volumen de trabajo, complejidad técnica y horas de desarrollo:

* **Walter Gonzalez (25%):** Responsable único y absoluto de **todo el CSS del proyecto** (arquitectura modular `estilos.css`, `componentes.css` y `responsive.css`), microinteracciones, accesibilidad visual, y de la **selección, curaduría y optimización del 100% de las imágenes reales de las 15 canchas y del set completo de iconos vectoriales SVG oficiales**.
* **Jose Sanchez (25%):** Responsable de la **maquetación y estructura HTML5 semántica de las vistas públicas y catálogo**: `index.html` (Landing institucional), `catalogo.html` (Catálogo con 15 instalaciones y filtros facetados) y `normas.html` (Reglamento de calzado y FAQ).
* **Jose Rozette (25%):** Responsable de la **maquetación y estructura HTML5 semántica de las vistas transaccionales del cliente**: `detalle.html` (Ficha técnica y matriz semanal de disponibilidad), `reservas.html` (Historial de turnos con desglose de abono del 30%) y `contacto.html` (Soporte y atención).
* **Alexander Meneses (25%):** Responsable de la **maquetación y estructura HTML5 semántica del módulo de autenticación y gestión administrativa**: `login.html` (Acceso/registro con pestañas CSS puro) y `admin.html` (Panel de Control, canchas precargadas, validación de abonos y cobro presencial POS).

### Declaración del Uso de Inteligencia Artificial (IA) en la Fase 3

En estricto apego al marco ético institucional de la Universidad Tecnológica de Panamá, declaramos que las herramientas de IA (Antigravity IDE / Google Gemini) fueron utilizadas como un **asistente técnico de soporte y optimización de código**, con los siguientes alcances específicos:
1. **Corrección de botones y navegación nativa:** Resolución de fallos en botones, enlaces y modales que dependían originalmente de eventos JavaScript, sustituyéndolos por patrones nativos de HTML5 y selectores CSS (`:target`, enlaces ancla y botones de envío).
2. **Unificación y saneamiento del DOM:** Fusión y reorganización de contenedores `<div>` que se encontraban innecesariamente fragmentados o separados en las tarjetas y tablas, consolidando una jerarquía limpia y semántica con etiquetas estándar (`<header>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`).
3. **Propuesta arquitectónica de archivos:** Asesoría técnica para descomponer la estructura de estilos monolítica previa hacia una organización modular limpia (`estilos.css`, `componentes.css`, `responsive.css`), facilitando la mantenibilidad y escalabilidad del código.
4. **Recomendación de fuentes de inspiración y diseño UI:** Sugerencia de plataformas de referencia visual (como Uiverse.io y repositorios de accesibilidad web) para la inspiración y concepción de botones modernos, tarjetas con esquinas redondeadas y microinteracciones hover enriquecidas con sombras verdes personalizadas.
