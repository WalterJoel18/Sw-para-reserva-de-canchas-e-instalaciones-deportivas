# Registro de Consultas y Uso de Asistentes IA

El siguiente documento recopila los prompts representativos utilizados durante el análisis, estructuración técnica y maquetación de los entregables del proyecto, registrando la interacción con los entornos de desarrollo asistido (Gemini / Antigravity IDE).

---

## Fase 1: Definición y Modelado Web

### Consulta 1: Sintaxis y Cardinalidad en Mermaid

* **Herramienta:** Gemini / Antigravity IDE
* **Objetivo:** Generar la estructura base en sintaxis Mermaid para el modelo de clases y navegación.
* **Prompt representativo:**
  > "Tengo las clases Usuario, Cancha, Horario, Reserva y CodigoAcceso con sus respectivos atributos y métodos del sistema. Genera la sintaxis Mermaid de tipo classDiagram respetando que Usuario realiza Reservas (1 a N), Cancha se asocia a Reservas y Horarios (1 a N), y CodigoAcceso valida al Administrador."
* **Uso y aporte intelectual:** Se tomó la sintaxis del diagrama generada como plantilla inicial y se corrigieron manualmente los tipos de datos, visibilidad de métodos y cardinalidades para adecuarlos a los requisitos del sistema.

### Consulta 2: Estructuración y Tabulación de Requisitos

* **Herramienta:** Gemini / Antigravity IDE
* **Objetivo:** Maquetación limpia en Markdown de las matrices de requisitos y escenarios.
* **Prompt representativo:**
  > "Organiza los requisitos funcionales (RF-01 a RF-09) y los escenarios de uso en tablas de Markdown limpias con columnas para código, módulo, descripción y rol de usuario asignado."
* **Uso y aporte intelectual:** Se adoptó la disposición en tablas Markdown para mantener una presentación uniforme en el README del repositorio.

---

## Fase 2: Arquitectura de Información y Navegación

### Consulta 3: Desacoplamiento de Dimensiones en el Catálogo

* **Herramienta:** Antigravity IDE / Gemini
* **Objetivo:** Normalizar la taxonomía de instalaciones deportivas para evitar filtros redundantes.
* **Prompt representativo:**
  > "En el catálogo de canchas tengo fútbol, fútbol sala, pádel y tenis mezclando superficie y modalidad. Ayúdame a separar conceptualmente estas variables para que sirvan tanto para filtros facetados como para atributos de base de datos."
* **Uso y aporte intelectual:** Se estableció la taxonomía multidimensional en cuatro ejes independientes (disciplina, modalidad, superficie y entorno), integrándola en la sección 1.2 B del informe.

### Consulta 4: Depuración Arquitectónica del Sitemap

* **Herramienta:** Antigravity IDE / Gemini
* **Objetivo:** Separar la jerarquía de páginas navegables de los componentes de interacción en capa de UI.
* **Prompt representativo:**
  > "Revisa este borrador de Sitemap. Necesito que los modales (como confirmación de reserva o cancelación) no se representen como páginas de navegación con URL independiente, sino como interacciones sobrepuestas en las pantallas de nivel 2."
* **Uso y aporte intelectual:** Se depuró el árbol jerárquico del Sitemap para dejar exclusivamente rutas navegables (`1.0` a `8.2`), reubicando los modales como componentes contextuales de Nivel 3.
