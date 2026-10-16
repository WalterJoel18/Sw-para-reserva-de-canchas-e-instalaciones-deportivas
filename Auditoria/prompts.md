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


### Consulta 9: Ampliación de Disciplinas, Canchas y Normativa de Equipamiento

* **Integrante:** Gonzalez, Walter
* **Herramienta:** Gemini / Antigravity IDE
* **Objetivo:** Ampliar el catálogo de instalaciones a 6 disciplinas (Fútbol, Básquetbol, Tenis, Pádel, Voleibol y Bádminton) y 9 tipologías de cancha, estructurando normativas técnicas de calzado según superficie.
* **Prompt representativo:**
  > "Necesitamos incorporar más deportes e instalaciones al complejo: fútbol sintético, fútbol sala techado, básquetbol de cemento y techado, tenis, pádel, voleibol de cemento y al aire libre, y bádminton. Ayúdame a definir la normativa de calzado y equipamiento por tipo de superficie (tabloncillo non-marking, césped sintético, concreto, etc.) y a desacoplar la taxonomía en 4 dimensiones."
* **Uso y aporte intelectual:** Se estructuraron las especificaciones técnicas y requerimientos de indumentaria por superficie en la sección 1.1 A, y se normalizó la taxonomía multidimensional en la sección 1.2 B para sustentar el catálogo ampliado de 9 canchas.

### Consulta 10: Lógica de Abonos, Política TTL para Reservas Fantasma y Regla de Cancelación

* **Integrante:** Gonzalez, Walter
* **Herramienta:** Gemini / Antigravity IDE
* **Objetivo:** Resolver el vacío operativo de reservas sin pasarela web, diseñar la política de caducidad temporal para turnos no abonados e insertar el rombo de 2 horas en la cancelación.
* **Prompt representativo:**
  > "El alcance del proyecto descarta pasarelas de pago externas. ¿Cómo modelamos la reserva web en estado Pendiente para que el cliente transfiera el abono por Yappy y envíe el comprobante por WhatsApp antes de que el administrador la confirme? Además, ¿cómo evitamos reservas fantasma que bloqueen turnos indefinidamente (política TTL), y cómo ajustamos el Flujo 2 en Mermaid para verificar la regla de más de 2 horas antes de cancelar?"
* **Uso y aporte intelectual:** Se diseñó el ciclo de estados de la reserva (Pendiente -> Confirmada -> Completada), la política Time-To-Live (TTL de 45 min) con liberación automática de bloques en la sección 1.4 C, el desglose de 4 importes en la tarjeta de reserva (1.1 B), y se incorporó el nodo de decisión de 2 horas en el diagrama Mermaid del Flujo 2 (RF-08).

### Consulta 11: Módulo POS de Liquidación en Sitio y Modelado del Flujo 6

* **Integrante:** Gonzalez, Walter
* **Herramienta:** Gemini / Antigravity IDE
* **Objetivo:** Diseñar la interacción del cobro presencial en ventanilla y modelar el Flujo 6 en Mermaid para completar el ciclo de vida de la reserva.
* **Prompt representativo:**
  > "Cuando el cliente se presenta a jugar adeuda el saldo restante. Necesito diseñar un modal tipo punto de venta (POS) para el recepcionista que permita cobrar en efectivo o Yappy presencial y transicionar la reserva a Completada, y generar el diagrama de flujo Mermaid paso a paso (Flujo 6)."
* **Uso y aporte intelectual:** Se incorporó el Modal de Liquidación en Sitio (POS) en los modales de Nivel 3 (sección 1.3), se añadieron las etiquetas operativas en 1.4 A, y se construyó el Flujo 6 completo con su ficha técnica y diagrama de decisión en la sección 4.6.

### Consulta 12: Refinamiento de Reglas de Negocio, Eliminación de CRUD de Canchas y Coherencia de Estados

* **Integrante:** Gonzalez, Walter
* **Herramienta:** Gemini / Antigravity IDE
* **Objetivo:** Adecuar el sistema a canchas precargadas (sin CRUD ni pantalla 8.1.1), fijar el abono al 30 %, formalizar la regla estricta de 2 horas (bloqueando creación/cancelación con 2 horas o menos), incluir el motivo de cancelación en el Flujo 2, separar el cobro POS del cierre del turno (Completada al terminar el partido), y unificar el estado Cancelada con motivo Vencimiento del TTL.
* **Prompt representativo:**
  > "Necesito ajustar la Fase 2 para que sea 100% coherente: elimina cualquier mención de CRUD o agregar/editar canchas (las canchas vienen precargadas y el admin solo conmuta Activa/Inactiva, eliminando la pantalla 8.1.1). Fija el abono al 30% como valor fijo del sistema. Cierra la regla de anticipación a 'no permite crear ni cancelar reservas cuando faltan 2 horas o menos' e incluye el paso de registrar el motivo de cancelación en el Flujo 2. En el POS y reserva asistida, separa el cobro presencial (el saldo queda en 0 y se emite comprobante) de la finalización del turno (pasa a Completada cuando el partido termina). Finalmente, unifica que el TTL deja la reserva en estado Cancelada con motivo Vencimiento del TTL."
* **Uso y aporte intelectual:** Se depuró la arquitectura de información eliminando la pantalla 8.1.1 en sitemap y navegación, se rediseñó el Flujo 3 para alternancia de estado con toggle switch, se ajustaron los diagramas Mermaid de los flujos 2, 5 y 6, y se normalizaron los textos normativos de anticipación y estados en todo el documento.

### Consulta 13: Aclaración de TTL y Validación, Regla Estricta de Cancelación, Diferenciación de Comprobantes, Desglose por Duración y Estructura de Secciones

* **Integrante:** Gonzalez, Walter
* **Herramienta:** Gemini / Antigravity IDE
* **Objetivo:** Perfeccionar la regla operativa del TTL (la reserva permanece Pendiente hasta que el administrador valide el abono; si no se valida en el TTL, se cancela y libera el horario), unificar la regla cerrada de cancelación («Cancelable únicamente si faltan más de 2 horas; a las 2 horas exactas o menos no se permite»), diferenciar formalmente la constancia de abono del comprobante de liquidación final, desglosar las tarifas según la duración seleccionada (1 hora vs. 2 horas), e integrar formalmente las Secciones 5 (Wireframes), 6 (Prototipo con enlace a Figma) y 7 (Auditoría) conforme a la rúbrica oficial.
* **Prompt representativo:**
  > "Ajusta la regla del TTL para que quede inequívoca: la reserva permanece Pendiente hasta que el administrador valide el abono; si no queda Confirmada dentro del TTL, se cancela y se libera el horario, aclarando qué pasa si el comprobante se envía a tiempo pero no se valida antes de expirar. Cambia 'Cancelable hasta 2 h' por 'Cancelable únicamente si faltan más de 2 horas; a las 2 horas exactas o menos no se permite'. Distingue formalmente el comprobante de abono (constancia) del comprobante de liquidación final (saldo en $0.00). Indica que el desglose económico depende de la duración del turno y da ejemplos para 1 y 2 horas. Finalmente, estructura formalmente la Sección 5 de Wireframes y la Sección 6 de Prototipo de Interfaz con su enlace a Figma, cerrando con la Sección 7 de Auditoría según la rúbrica oficial."
* **Uso y aporte intelectual:** Se actualizaron las especificaciones en las secciones 1.1, 1.3, 1.4, 2.2, y 4 (Flujos 1 y 2), y se redactaron formalmente las secciones 5 (Wireframes), 6 (Prototipo de Interfaz en Figma) y 7 (Auditoría y Declaración de IA con Tabla 3), asegurando la concordancia total entre el documento escrito, los wireframes y el prototipo interactivo.
