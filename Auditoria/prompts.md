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

### Consulta 5: Accesibilidad Universal en Disponibilidad (WCAG 2.1 AA) y Diseño Móvil

* **Herramienta:** Antigravity IDE / Gemini
* **Objetivo:** Definir la regla multimodal para los indicadores de estado del calendario y la solución responsiva para pantallas móviles.
* **Prompt representativo:**
  > "Para la matriz de disponibilidad de horarios de las canchas, ¿cómo garantizo que los estados libre, ocupado y mantenimiento cumplan con el estándar de accesibilidad WCAG 2.1 Nivel AA para usuarios con daltonismo, y cómo debe adaptarse la cuadrícula en dispositivos móviles para no requerir scroll horizontal?"
* **Uso y aporte intelectual:** Se adoptó la estrategia de señalización multimodal combinando color de alto contraste (4.5:1), texto explícito e iconografía etiquetada, junto con el colapso responsivo a un carrusel selector de fecha con lista vertical de bloques en móviles, incorporándolo en la sección 1.4 B del informe.

### Consulta 6: Manejo de Concurrencia y Validación Transaccional en Agendamiento

* **Herramienta:** Antigravity IDE / Gemini
* **Objetivo:** Diseñar el mecanismo de control de colisiones de turnos para condiciones de carrera en la reserva web.
* **Prompt representativo:**
  > "Necesito modelar qué ocurre si dos usuarios intentan confirmar la misma cancha en el mismo horario simultáneamente. ¿Cómo justificamos técnicamente la verificación en dos pasos y el manejo de condiciones de carrera a nivel de arquitectura web para que sea coherente con el flujo alterno de casos de uso?"
* **Uso y aporte intelectual:** Se diseñó la regla de validación transaccional inmediata en el servidor previa al registro (`COMMIT`), definiendo el mensaje de excepción controlado y la actualización automática de la vista, integrándolo en la sección 1.4 C y en el rombo de decisión del Flujo 1.

### Consulta 7: Estructuración y Bifurcaciones de Flujos de Tareas Críticas

* **Integrante:** Sanchez, Jose
* **Herramienta:** Gemini
* **Objetivo:** Estructurar el paso a paso secuencial de los flujos de navegación incorporando bifurcaciones lógicas y manejo de excepciones.
* **Prompt representativo:**
  > "Tengo los escenarios de agendamiento y cancelación de reservas del sistema de canchas. Ayúdame a estructurar el flujo paso a paso (entre 5 y 7 pasos) en un diagrama de flujo lógico, incluyendo los rombos de decisión para cuando el usuario no tiene sesión activa o cuando fallan los datos del formulario."
* **Uso y aporte intelectual:** Se tomó la estructura lógica de bifurcaciones propuesta y se adaptaron manualmente los identificadores de pantallas (1.0 a 8.2), las precondiciones específicas y la conservación de datos en memoria para evitar pérdida de información.

### Consulta 8: Depuración de Inconsistencias y Casos Borde en Flujos Administrativos

* **Integrante:** Sanchez, Jose
* **Herramienta:** Gemini
* **Objetivo:** Limar impurezas, redundancias e incoherencias técnicas en los flujos de administración (bloqueo de canchas y reserva asistida).
* **Prompt representativo:**
  > "Revisa estos borradores de flujo para el panel de administración: bloqueo por mantenimiento y registro de reserva presencial o telefónica. Señala posibles incoherencias o pasos redundantes para que el flujo sea directo y contemple qué pasa si el horario ya fue reservado o si hay reservas activas en el rango."
* **Uso y aporte intelectual:** Se eliminaron pasos redundantes en la interacción administrativa y se incorporaron las validaciones de colisión de turnos y advertencia previa de reservas vigentes, vinculándolas formalmente con los casos de uso CU-08 y CU-09.

