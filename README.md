# UNIVERSIDAD TECNOLÓGICA DE PANAMÁ
## FACULTAD DE INGENIERÍA DE SISTEMAS COMPUTACIONALES
### DEPARTAMENTO DE INGENIERÍA DE SOFTWARE

**Materia:** Ingeniería Web  
**Grupo:** 1SF133  
**Docente:** Dra. Elba Valderrama Bahamóndez  
**Período:** II Semestre de 2026  
**Tema:** Proyecto Final (Fase 1) – Birrias de One: Sistema web para reserva de canchas e instalaciones deportivas  

**Integrantes:**
* Gonzalez, Walter — 8-1027-2220
* Sanchez, Jose — 8-1038-670
* Rozette, Jose — 8-1025-306
* Meneses, Alexander — 8-1035-623

---

### Avance del Proyecto
* **Enlace al repositorio (carpetas y estructura):** [https://github.com/WalterJoel18/Sw-para-reserva-de-canchas-e-instalaciones-deportivas](https://github.com/WalterJoel18/Sw-para-reserva-de-canchas-e-instalaciones-deportivas)
* **Enlace a la web (lectura del avance):** [https://walterjoel18.github.io/Sw-para-reserva-de-canchas-e-instalaciones-deportivas/](https://walterjoel18.github.io/Sw-para-reserva-de-canchas-e-instalaciones-deportivas/)

---

# Fase 1: Definición, Requisitos y Modelado Web

## 1. Descripción del proyecto

* **Nombre del Proyecto:** Birrias de One – Sistema web para reserva de canchas e instalaciones deportivas.
* **Problema o necesidad:** La dificultad y pérdida de tiempo que enfrentan los usuarios al intentar encontrar canchas disponibles debido a la falta de información centralizada. Asimismo, la ineficiencia de los administradores de los complejos deportivos al llevar el control de reservas, horarios y cancelaciones de manera manual.
* **Propósito:** Proporcionar un sistema digitalizado y centralizar la información respecto a la reserva de canchas.
* **Objetivo general:** Diseñar e implementar una página web centralizada que mejore la experiencia de los usuarios en la búsqueda y reserva de canchas deportivas, garantizando el acceso a información actualizada y detallada sobre las instalaciones en todo momento.
* **Alcance:** El proyecto abarcará el diseño y desarrollo de una aplicación web responsiva. Incluirá un catálogo digital de instalaciones deportivas con sus respectivos detalles (costos, ubicación, superficie y condiciones). Contará con un módulo de acceso público para consulta y disponibilidad, un módulo para clientes registrados (orientado a la generación de reservas con cálculo de abono mínimo sugerido) y un módulo administrativo (para control de estados, registro asistido y liquidación de reservas en sitio).
* **Principales funcionalidades (Consideradas hasta ahora):**
  * Registro y autenticación de usuarios (perfil cliente y perfil administrador).
  * Buscador de canchas con filtros por tipo de deporte y disponibilidad de fechas/horarios.
  * Calendario interactivo para visualizar horarios libres y ocupados en tiempo real.
  * Sistema de generación, confirmación y cancelación de reservas.
  * Panel de administración para agregar/editar la información de las canchas y gestionar el estado de las reservas.

---

## 2. Identificación de usuarios

### Cliente no registrado (Visitante)
* **Características:** Personas que acceden por primera vez al sitio web o usuarios recurrentes que no han iniciado sesión. Buscan conocer las instalaciones, comparar tarifas y verificar horarios libres antes de decidirse a crear una cuenta.
* **Necesidades:**
  * Explorar el catálogo completo de canchas y sus especificaciones técnicas.
  * Filtrar instalaciones por disciplina deportiva y rango de precios.
  * Consultar el calendario dinámico de disponibilidad en tiempo real.
* **Funciones principales en el sistema:**
  * Navegar en la página principal y catálogo.
  * Realizar búsquedas con filtros facetados.
  * Visualizar los bloques horarios libres y ocupados.
  * Ser redirigido al registro/inicio de sesión al intentar apartar un horario disponible.

### Cliente
* **Características:** Personas de diversas edades interesadas en practicar deportes o realizar actividades físicas. Por lo general, disponen de poco tiempo y buscan soluciones rápidas y convenientes.
* **Necesidades:**
  * Encontrar rápidamente una cancha disponible que se ajuste a su deporte, horario y presupuesto.
  * Conocer las características exactas de la instalación (ubicación, si es techada, tipo de piso, precio) antes de reservar.
  * Realizar una reserva de forma inmediata sin tener que hacer llamadas telefónicas, esperar confirmaciones por WhatsApp o ir presencialmente al lugar.
* **Funciones principales en el sistema:**
  * Registrarse e iniciar sesión.
  * Buscar y filtrar canchas (por deporte, fecha y hora).
  * Visualizar el calendario interactivo de disponibilidad.
  * Realizar la reserva de un horario específico.
  * Cancelar una reserva previamente hecha.
  * Ver su historial de reservas (pasadas y próximas).

### Administrador
* **Características:** Personal empleado por el complejo deportivo (recepcionistas, gerentes o dueños). Tienen conocimientos básicos o intermedios en el uso de sistemas informáticos y son los responsables directos de la atención al público, el cobro y el mantenimiento de las instalaciones.
* **Necesidades:**
  * Mantener un control organizado y centralizado de todas las reservas del día para evitar la sobreocupación de canchas (dos personas reservando la misma cancha).
  * Poder bloquear horarios si una cancha entra en reparación o mantenimiento.
  * Tener acceso a los datos de contacto del cliente en caso de que ocurra algún inconveniente con la reserva.
* **Funciones principales en el sistema:**
  * Iniciar sesión en un panel de control privado (Dashboard).
  * Gestionar el catálogo de instalaciones: editar la información de las canchas (precios, fotos, estado).
  * Visualizar un listado completo o calendario con todas las reservas agendadas por los clientes.
  * Cambiar el estado de las reservas.
  * Bloquear manualmente horarios de las canchas por motivos de cierre o mantenimiento.

---

## 3. Requisitos funcionales

| Código | Módulo | Descripción del Requisito | Usuario |
| :--- | :--- | :--- | :--- |
| **RF-01** | Seguridad | El sistema debe permitir a los usuarios registrarse ingresando sus datos personales (nombre, correo, teléfono y contraseña), asignando el rol de Cliente por defecto o el rol de Administrador si se introduce un código de acceso corporativo válido. | Visitante |
| **RF-02** | Seguridad | El sistema debe autenticar a los usuarios mediante correo y contraseña; tras validar las credenciales, debe redirigir al panel de administración si el rol es Administrador o al catálogo principal si el rol es Cliente. | Cliente / Administrador |
| **RF-03** | Catálogo | El sistema debe permitir al administrador consultar el catálogo de canchas, editar sus atributos (tarifas, condiciones, iluminación e imágenes) y modificar su estado a activo o inactivo. | Administrador |
| **RF-04** | Búsqueda | El sistema debe permitir buscar y filtrar canchas por disciplina deportiva, modalidad, tipo de superficie, ubicación y rango de precios. | Público |
| **RF-05** | Disponibilidad | El sistema debe presentar un calendario interactivo con la disponibilidad de cada cancha, diferenciando visualmente bloques libres, ocupados y bloqueados por mantenimiento. | Público |
| **RF-06** | Reservas | El sistema debe permitir al cliente seleccionar un bloque libre y generar una reserva en estado Pendiente, bloqueando inmediatamente el horario para evitar colisiones y mostrando el valor estimado de la reserva. | Cliente |
| **RF-07** | Perfil | El sistema debe permitir al cliente autenticado visualizar su historial de reservas, detallando cancha, fecha, rango horario, estado actual y valor estimado. | Cliente |
| **RF-08** | Reservas | El sistema debe permitir al cliente cancelar una reserva propia que se encuentre en estado Pendiente o Confirmada, siempre que falten más de 2 horas para su inicio, liberando el bloque horario automáticamente. | Cliente |
| **RF-09** | Gestión | El sistema debe permitir al administrador visualizar todas las reservas del complejo, registrar reservas realizadas de forma presencial o telefónica y actualizar su estado operativo: Confirmada, Cancelada o Completada. | Administrador |
| **RF-10** | Gestión | El sistema debe permitir al administrador consultar el valor estimado de cada reserva y registrar una observación relacionada con el pago presencial, sin procesar pagos dentro de la plataforma. | Administrador |
| **RF-11** | Mantenimiento | El sistema debe permitir al administrador bloquear rangos específicos de fechas y horas en una cancha por motivos de mantenimiento o cierre, impidiendo nuevas reservas en esos intervalos. | Administrador |

---

## 4. Requisitos no funcionales

| Código | Categoría | Descripción del Requisito |
| :--- | :--- | :--- |
| **RNF-01** | Usabilidad | La interfaz debe ser intuitiva, permitiendo que un usuario nuevo realice una reserva sin necesitar capacitación previa. |
| **RNF-02** | Responsive | El sistema debe adaptarse correctamente a dispositivos móviles, tablets y computadoras de escritorio. |
| **RNF-03** | Seguridad | Las contraseñas deben almacenarse mediante funciones de hash y las sesiones deben protegerse contra accesos no autorizados. |
| **RNF-04** | Rendimiento | El sistema debe cargar el calendario de disponibilidad en un máximo de 3 segundos bajo condiciones normales de red. |
| **RNF-05** | Disponibilidad | La plataforma debe permitir a los clientes consultar la disponibilidad y realizar reservas siempre que el sistema se encuentre operativo. |
| **RNF-06** | Compatibilidad | El sistema debe funcionar correctamente en los navegadores más usados (Chrome, Firefox, Edge y Safari). |
| **RNF-07** | Escalabilidad | El sistema debe permitir agregar nuevas canchas deportivas sin requerir cambios importantes en la estructura del sistema. |
| **RNF-08** | Mantenibilidad | El código debe estar documentado y modularizado para facilitar futuras actualizaciones o correcciones. |

---

## 5. Escenarios de uso

| Usuario | Objetivo | Contexto | Secuencia | Resultado esperado |
| :--- | :--- | :--- | :--- | :--- |
| **Visitante / Administrador** | Registrarse en el sistema | Un usuario nuevo o empleado del complejo desea crear una cuenta por primera vez. | Accede al formulario de registro → ingresa nombre, correo, teléfono, contraseña (y opcionalmente código corporativo de empleado) → confirma el registro. | Se crea la cuenta con el rol correspondiente ('Cliente' por defecto o 'Administrador' si el código es válido) y queda habilitado para iniciar sesión. |
| **Visitante / Cliente** | Consultar catálogo, filtros y disponibilidad | Una persona desea conocer las canchas disponibles, tarifas, especificaciones técnicas y horarios libres antes de decidir apartar un turno. | Ingresa a la página principal → aplica filtros facetados (deporte, modalidad, horario, precio) → abre la ficha de la cancha → revisa el calendario interactivo. | Visualiza las canchas filtradas y los horarios libres/ocupados en tiempo real sin requerir inicio de sesión previo. |
| **Cliente / Administrador** | Iniciar sesión en la plataforma | Usuario registrado necesita acceder a sus funciones según su rol. | Ingresa a Inicio de Sesión → introduce correo y contraseña → el sistema valida credenciales y evalúa el rol del usuario. | El sistema autentica al usuario; redirige al Cliente al catálogo principal y al Administrador al Dashboard administrativo. |
| **Cliente** | Agendar reserva con abono mínimo | Cliente autenticado desea apartar una cancha para el fin de semana. | Selecciona una cancha y un bloque horario libre en el calendario → revisa el resumen con tarifa total y abono mínimo estimado → confirma la solicitud. | Se genera la reserva en estado **Pendiente**, el horario se bloquea de inmediato para evitar colisiones y se despliegan los datos para depositar el abono. |
| **Cliente** | Cancelar reserva oportunamente | Un cliente con reserva no podrá asistir al partido agendado. | Accede a "Mis reservas" → selecciona una reserva activa con más de 2 horas de anticipación → presiona "Cancelar" → confirma la acción. | La reserva cambia a estado **Cancelada**, se registra el motivo de cancelación y el horario vuelve a estar disponible inmediatamente en el calendario. |
| **Cliente** | Consultar historial y estado de reservas | El cliente quiere revisar sus reservas activas, solicitudes pendientes y partidos pasados. | Inicia sesión → accede a la sección "Mis reservas / Historial" → visualiza el listado detallado con estado, abono registrado y saldo pendiente. | El cliente comprueba el estatus de sus reservas y el detalle de cada turno. |
| **Administrador** | Confirmar reserva pendiente | El administrador debe validar una reserva creada por un cliente tras verificar el abono recibido. | Accede al listado de reservas → filtra por estado 'Pendiente' → valida el comprobante del abono (vía recepción/Yappy) → cambia su estado a 'Confirmada'. | La reserva pasa a estado **Confirmada** y el cambio se refleja inmediatamente en el perfil del cliente. |
| **Administrador** | Registrar reserva asistida | Un cliente acude en persona a la recepción o llama por teléfono para apartar cancha sin usar la web directamente. | Accede al calendario administrativo → selecciona un bloque horario libre → ingresa los datos de contacto del cliente y el abono inicial recibido → guarda la reserva. | Se crea la reserva directamente en estado **Confirmada**, bloqueando el horario y asociando el turno al cliente. |
| **Administrador** | Liquidar y completar reserva en ventanilla | Los jugadores finalizaron el uso de la cancha o se presentan a liquidar el turno en recepción. | Selecciona la reserva confirmada → el sistema calcula automáticamente `Total - Abono = Saldo Pendiente` → admin recibe el pago completo en caja y marca el turno como 'Completada'. | La reserva finaliza en estado **Completada**, queda cerrada y el sistema genera el comprobante digital de liquidación. |
| **Administrador** | Editar información y disponibilidad de canchas | El administrador necesita actualizar precios, reglas de calzado o pausar temporalmente una cancha del catálogo. | Accede a gestión de canchas → selecciona la instalación → edita tarifas/condiciones o conmuta su estado a "Inactiva" (desactivación lógica) → guarda cambios. | El catálogo público se actualiza reflejando la nueva información o retirando la cancha de la búsqueda sin borrar su historial transaccional. |
| **Administrador** | Bloquear horarios por mantenimiento | Una cancha presenta daños, lluvia o mantenimiento preventivo de luminarias/césped. | Accede a la gestión de la cancha → selecciona la opción "Bloquear horarios" → indica el rango de fecha y horas → confirma bloqueo. | Los horarios seleccionados quedan inhabilitados en el calendario (color gris/bloqueado) impidiendo nuevas reservas. |

---

## 6. Casos de uso

### 6.1 Diagrama de casos de uso

```mermaid
flowchart LR
    %% Estilos UML
    classDef actor fill:transparent,stroke:transparent,color:#000,font-size:16px;
    classDef usecase fill:#2C52D1,stroke:#111,stroke-width:1px,color:#fff;

    %% Actores
    Visitante["👤<br/>Visitante"]:::actor
    Cliente["🏃<br/>Cliente"]:::actor
    Admin["👔<br/>Administrador"]:::actor

    %% Relación de herencia / especialización en flowchart
    Cliente -.-> Visitante

    %% Sistema
    subgraph Sistema ["Sistema Birrias de One"]
        direction TB
        CU01(["CU-01: Registrarse en el sistema"]):::usecase
        CU02(["CU-02: Iniciar sesión unificado"]):::usecase
        CU03(["CU-03: Buscar canchas con filtros"]):::usecase
        CU04(["CU-04: Visualizar disponibilidad de horarios"]):::usecase
        CU05(["CU-05: Reservar cancha - Pendiente"]):::usecase
        CU06(["CU-06: Cancelar reserva"]):::usecase
        CU07(["CU-07: Consultar historial de reservas"]):::usecase
        CU08(["CU-08: Administrar información de canchas"]):::usecase
        CU09(["CU-09: Gestionar reservas y registro asistido"]):::usecase
        CU10(["CU-10: Bloquear horarios por mantenimiento"]):::usecase
        CU11(["CU-11: Liquidar reserva y emitir comprobante"]):::usecase
    end

    %% Interacciones de Visitante
    Visitante --- CU01
    Visitante --- CU02
    Visitante --- CU03
    Visitante --- CU04

    %% Interacciones de Cliente
    Cliente --- CU05
    Cliente --- CU06
    Cliente --- CU07

    %% Interacciones de Administrador
    CU02 --- Admin
    CU08 --- Admin
    CU09 --- Admin
    CU10 --- Admin
    CU11 --- Admin

    style Sistema fill:transparent,stroke:#000,stroke-width:2px
```

---

### 6.2 Descripción de los principales casos de uso

#### CU-01: Registrarse en el sistema
| Campo | Descripción |
| :--- | :--- |
| **Código** | CU-01 |
| **Nombre** | Registrarse en el sistema |
| **Actor(es)** | Cliente, Administrador |
| **Precondición** | El usuario no tiene una cuenta en el sistema. |
| **Flujo principal** | 1. El usuario accede a la página de registro. <br> 2. Completa los campos: nombre, correo, teléfono y contraseña. <br> 3. (Opcional) Ingresa un código de acceso de empleado. <br> 4. El sistema valida que el correo no esté registrado. <br> 5. El sistema crea la cuenta con el rol correspondiente. <br> 6. Se muestra un mensaje de confirmación. |
| **Flujo alterno** | 4a. Si el correo ya está registrado, el sistema muestra un error. <br> 5a. Si el código de empleado es incorrecto, el sistema rechaza el rol de administrador. |
| **Postcondición** | La cuenta queda creada y el usuario puede iniciar sesión. |

#### CU-02: Iniciar sesión
| Campo | Descripción |
| :--- | :--- |
| **Código** | CU-02 |
| **Nombre** | Iniciar sesión |
| **Actor(es)** | Cliente, Administrador |
| **Precondición** | El usuario tiene una cuenta registrada en el sistema. |
| **Flujo principal** | 1. El usuario accede a la página de inicio de sesión. <br> 2. Ingresa su correo y contraseña. <br> 3. El sistema valida las credenciales. <br> 4. Si el rol es "Cliente", se redirige a la página principal del catálogo. <br> 5. Si el rol es "Administrador", se redirige al panel de gestión. |
| **Flujo alterno** | 3a. Si las credenciales son incorrectas, el sistema muestra un error de autenticación. |
| **Postcondición** | El usuario accede al sistema con los permisos de su rol. |

#### CU-03: Buscar canchas con filtros
| Campo | Descripción |
| :--- | :--- |
| **Código** | CU-03 |
| **Nombre** | Buscar canchas con filtros |
| **Actor(es)** | Visitante, Cliente |
| **Precondición** | Acceso público (no requiere inicio de sesión). |
| **Flujo principal** | 1. El usuario accede al buscador de canchas. <br> 2. Aplica los filtros deseados: tipo de deporte, fecha, horario y/o precio. <br> 3. El sistema consulta la base de datos y devuelve resultados. <br> 4. Se muestran las canchas que cumplen con los criterios. |
| **Flujo alterno** | 3a. Si no se encuentran canchas, se sugiere eliminar algunos filtros. |
| **Postcondición** | El usuario visualiza una lista de canchas acordes a su búsqueda. |

#### CU-04: Visualizar disponibilidad de horarios
| Campo | Descripción |
| :--- | :--- |
| **Código** | CU-04 |
| **Nombre** | Visualizar disponibilidad de horarios |
| **Actor(es)** | Visitante, Cliente |
| **Precondición** | El usuario ha seleccionado una cancha específica. |
| **Flujo principal** | 1. El usuario entra a ver los detalles de la cancha. <br> 2. El sistema muestra un calendario interactivo. <br> 3. Los horarios libres se muestran en color verde y los ocupados en rojo. |
| **Flujo alterno** | 2a. Si la cancha no tiene horarios disponibles para esa fecha, se sugiere cambiar de día. |
| **Postcondición** | El usuario identifica qué horarios están libres para reservar. |

#### CU-05: Reservar una cancha
| Campo | Descripción |
| :--- | :--- |
| **Código** | CU-05 |
| **Nombre** | Reservar una cancha |
| **Actor(es)** | Cliente |
| **Precondición** | El cliente visualizó un horario libre y cuenta con sesión activa. |
| **Flujo principal** | 1. El cliente hace clic sobre un bloque horario disponible (en verde). <br> 2. El sistema calcula y presenta la pantalla de confirmación con el resumen: cancha, fecha, rango de horas, tarifa total calculada y monto del abono mínimo sugerido para asegurar el turno. <br> 3. El cliente confirma la reserva. <br> 4. El sistema guarda la reserva asignándole el estado Pendiente y bloquea automáticamente el horario en el calendario de la cancha. <br> 5. Se emite en pantalla el mensaje de confirmación con el número de reserva e instrucciones para el depósito del abono en la recepción o vía electrónica. |
| **Flujo alterno** | 4a. Si otro cliente reservó el mismo bloque un instante antes (conflicto), el sistema informa y solicita seleccionar otro horario. |
| **Postcondición** | La reserva queda registrada en estado Pendiente y el horario bloqueado para otros. |

#### CU-06: Cancelar una reserva
| Campo | Descripción |
| :--- | :--- |
| **Código** | CU-06 |
| **Nombre** | Cancelar una reserva |
| **Actor(es)** | Cliente |
| **Precondición** | El cliente tiene una reserva activa (Pendiente o Confirmada). |
| **Flujo principal** | 1. El cliente ingresa a su sección "Mis Reservas". <br> 2. Selecciona la reserva que necesita suspender y presiona "Cancelar Reserva". <br> 3. El sistema valida la regla de negocio temporal: verifica que falten más de 2 horas respecto a la hora pactada de inicio. <br> 4. El sistema solicita confirmación. <br> 5. El cliente confirma la cancelación. <br> 6. El sistema cambia el estado de la reserva a Cancelada, registra la fecha de cancelación y libera el horario inmediatamente en el calendario. |
| **Flujo alterno** | 3a. Si faltan menos de 2 horas para el inicio del turno, el sistema deshabilita la acción y muestra: "No es posible cancelar en línea con menos de 2 horas de anticipación. Por favor comuníquese con la administración". |
| **Postcondición** | El horario vuelve a estar disponible para el público. |

#### CU-07: Consultar historial de reservas
| Campo | Descripción |
| :--- | :--- |
| **Código** | CU-07 |
| **Nombre** | Consultar historial de reservas |
| **Actor(es)** | Cliente |
| **Precondición** | El cliente ha iniciado sesión. |
| **Flujo principal** | 1. El cliente ingresa a la sección "Historial". <br> 2. El sistema muestra las reservas pasadas y futuras con su estado actual (completada, cancelada, confirmada). |
| **Flujo alterno** | 2a. Si el cliente no tiene reservas, se muestra un mensaje informativo vacío. |
| **Postcondición** | El cliente queda informado sobre toda su actividad en la plataforma. |

#### CU-08: Gestionar canchas (CRUD)
| Campo | Descripción |
| :--- | :--- |
| **Código** | CU-08 |
| **Nombre** | Gestionar canchas (CRUD) |
| **Actor(es)** | Administrador |
| **Precondición** | El administrador ha iniciado sesión en el panel de gestión. |
| **Flujo principal** | 1. El administrador accede al catálogo interno de canchas. <br> 2. Puede Agregar, Editar o Desactivar una cancha. <br> 3. Ingresa o modifica los datos y guarda. <br> 4. El sistema valida y actualiza la base de datos. |
| **Flujo alterno** | 4a. Faltan datos obligatorios al guardar. El sistema bloquea la operación y pide completarlos. |
| **Postcondición** | El catálogo público de canchas queda actualizado con los cambios. |

#### CU-09: Gestionar el estado de las reservas
| Campo | Descripción |
| :--- | :--- |
| **Código** | CU-09 |
| **Nombre** | Gestionar el estado de las reservas |
| **Actor(es)** | Administrador |
| **Precondición** | Existen reservas registradas por los clientes. |
| **Flujo principal** | 1. El administrador abre la lista general de reservas. <br> 2. Selecciona una reserva y cambia su estado a «Completada» o «Cancelada». <br> 3. Guarda los cambios. <br> 4. El sistema actualiza el estado en la base de datos. |
| **Flujo alterno** | 1a. Si no hay reservas registradas, el sistema indica que no existen reservas para gestionar. |
| **Postcondición** | Los estados de las reservas quedan actualizados y se reflejan en el historial del cliente. |

#### CU-10: Bloquear horarios por mantenimiento
| Campo | Descripción |
| :--- | :--- |
| **Código** | CU-10 |
| **Nombre** | Bloquear horarios por mantenimiento |
| **Actor(es)** | Administrador |
| **Precondición** | El administrador ha iniciado sesión en el sistema. |
| **Flujo principal** | 1. El administrador selecciona la cancha que necesita reparación. <br> 2. Selecciona el rango de fechas y horas a bloquear. <br> 3. Confirma y guarda. <br> 4. El sistema marca esos bloques como no disponibles para los clientes. |
| **Flujo alterno** | 3a. Ya existen reservas en el horario seleccionado. El sistema advierte que debe resolver las reservas existentes antes de bloquear. |
| **Postcondición** | Los horarios seleccionados quedan inhabilitados en el calendario público. |

#### CU-11: Liquidar reserva y emitir comprobante
| Campo | Descripción |
| :--- | :--- |
| **Código** | CU-11 |
| **Nombre** | Liquidar reserva y emitir comprobante |
| **Actor(es)** | Administrador |
| **Precondición** | La reserva se encuentra en estado confirmada y los jugadores se presentan al complejo. |
| **Flujo principal** | 1. El administrador localiza la reserva en el sistema al presentarse el cliente al partido. <br> 2. Selecciona la opción "Liquidar / Cobro de Turno". <br> 3. El sistema calcula automáticamente los valores económicos: `Tarifa Total - Abono Registrado = Saldo Pendiente`. <br> 4. El administrador recibe el cobro presencial por el monto del saldo pendiente y presiona "Confirmar Pago Total". <br> 5. El sistema actualiza el estado de la reserva a Completada y registra el cobro total. <br> 6. El sistema genera en pantalla un comprobante digital de liquidación con el desglose de conceptos, número de turno y confirmación de pago para visualización o impresión del cliente. |
| **Flujo alterno** | 4a. Si el usuario no abona el total restante, el sistema no permite el cierre del turno, manteniendo la reserva en estado confirmada hasta su liquidación íntegra. |
| **Postcondición** | La reserva queda cerrada como 'Completada' y se genera el recibo de liquidación. |

---

## 7. Modelo de clases

Este modelo representa las entidades principales, sus atributos, métodos y la forma en que se relacionan dentro del sistema.

```mermaid
classDiagram
    class Usuario {
        +int id_usuario
        +String nombre
        +String correo
        +String telefono
        +String contrasena_hash
        +String rol
        +Date fecha_registro
        +registrar()
        +iniciarSesion()
        +cerrarSesion()
    }

    class Cancha {
        +int id_cancha
        +String nombre
        +String deporte
        +String modalidad
        +String tipo_superficie
        +boolean iluminacion_techada
        +float precio_hora
        +String ubicacion
        +String condiciones
        +boolean activo
        +String imagen_url
        +editar()
        +conmutarEstado()
        +listar()
    }

    class Reserva {
        +int id_reserva
        +int id_usuario
        +int id_cancha
        +Date fecha
        +Time hora_inicio
        +Time hora_fin
        +float monto_total
        +float abono_minimo
        +float monto_abonado
        +float saldo_pendiente
        +String estado
        +Date fecha_creacion
        +crearReserva()
        +cancelarReserva()
        +confirmarReserva()
        +liquidarReserva()
        +consultarHistorial()
    }

    class Horario {
        +int id_horario
        +int id_cancha
        +Date fecha
        +Time hora_inicio
        +Time hora_fin
        +String estado_bloque
        +verificarDisponibilidad()
        +bloquearPorReserva()
        +bloquearPorMantenimiento()
        +liberarHorario()
    }

    class ComprobanteLiquidacion {
        +int id_comprobante
        +int id_reserva
        +Date fecha_emision
        +float total_pagado
        +String metodo_pago
        +String codigo_recibo
        +generarRecibo()
        +imprimir()
    }

    class CodigoAcceso {
        +int id_codigo
        +String codigo
        +boolean activo
        +Date fecha_creacion
        +validarCodigo()
    }

    Usuario "1" --> "*" Reserva : gestiona
    Cancha "1" --> "*" Reserva : es reservada en
    Cancha "1" --> "*" Horario : dispone de
    Reserva "1" --> "1" Horario : vincula
    Reserva "1" --> "1" ComprobanteLiquidacion : genera liquidacion
    CodigoAcceso ..> Usuario : autoriza rol admin
```

### Descripción de las clases del modelo

| Clase | Descripción |
| :--- | :--- |
| **Usuario** | Representa a cualquier persona registrada en el sistema (cliente o administrador). Almacena credenciales, datos personales y el rol asignado. |
| **Cancha** | Representa una instalación deportiva del complejo. Contiene toda la información visible para los clientes (nombre, deporte, precio, ubicación, condiciones y estado). |
| **Reserva** | Registra el vínculo entre un usuario y una cancha en un horario específico. Controla el ciclo de vida de la reserva (Pendiente, Confirmada, Completada o Cancelada). |
| **Horario** | Representa los bloques de tiempo disponibles para cada cancha. Permite al sistema gestionar la disponibilidad y aplicar bloqueos por mantenimiento. |
| **ComprobanteLiquidacion** | Entidad generada cuando el administrador finaliza y liquida la reserva en ventanilla, documentando el pago completo del saldo pendiente. |
| **CodigoAcceso** | Almacena los códigos secretos que permiten a los trabajadores del complejo registrarse con permisos de administrador. |

---

## 8. Modelo de navegación inicial

Diagrama que muestra la estructura del sitio y cómo los usuarios interactúan y se desplazan entre las pantallas principales de la aplicación.

```mermaid
flowchart TD
    Inicio["Portal Publico - Landing"]
    CatPub["Catalogo y Disponibilidad Publica"]
    Reg["Registro de Cuenta"]
    Login["Inicio de Sesion"]
    ValidaRol{"¿Rol del Usuario?"}

    %% Vistas Cliente
    CatCli["Catalogo de Canchas"]
    DetCancha["Ficha Tecnica de Cancha"]
    Calen["Calendario de Disponibilidad"]
    ResumenRes["Resumen con Abono Minimo"]
    Confirmada["Turno en Estado Pendiente"]
    MisRes["Mis Reservas e Historial"]
    CancelaModal["Cancelar Reserva - Limite 2h"]

    %% Vistas Administrador
    DashAdmin["Dashboard Administrativo"]
    GestionCanchas["Edicion y Desactivacion de Canchas"]
    ListadoRes["Control Global de Reservas"]
    ReservaAsistida["Registro Asistido de Turno"]
    LiquidarModal["Liquidacion y Cobro de Saldo"]
    ComprobanteView["Comprobante de Turno Completado"]
    BloqueoMantenimiento["Bloqueo Preventivo de Horarios"]

    %% Flujos de Navegacion
    Inicio --> CatPub
    Inicio --> Reg
    Inicio --> Login

    CatPub --> DetCancha
    DetCancha --> Calen
    Calen -->|Requiere Login para Reservar| Login

    Reg --> Login
    Login --> ValidaRol

    ValidaRol -->|Rol: Cliente| CatCli
    ValidaRol -->|Rol: Administrador| DashAdmin

    CatCli --> DetCancha
    DetCancha --> Calen
    Calen -->|Selecciona Horario Libre| ResumenRes
    ResumenRes --> Confirmada
    Confirmada --> MisRes
    MisRes --> CancelaModal

    DashAdmin --> GestionCanchas
    DashAdmin --> ListadoRes
    DashAdmin --> BloqueoMantenimiento
    ListadoRes --> ReservaAsistida
    ListadoRes --> LiquidarModal
    LiquidarModal --> ComprobanteView

    style Inicio fill:#6C3483,stroke:#4A235A,color:#fff
    style ValidaRol fill:#F39C12,stroke:#D68910,color:#fff
    style CatCli fill:#2980B9,stroke:#1A5276,color:#fff
    style DashAdmin fill:#E74C3C,stroke:#922B21,color:#fff
    style ComprobanteView fill:#27AE60,stroke:#1E8449,color:#fff
```

### Descripción de pantallas principales

| Pantalla | Descripción | Usuario |
| :--- | :--- | :--- |
| **Página de Inicio** | Landing page pública con el acceso al registro e inicio de sesión. | Público |
| **Inicio de Sesión / Registro** | Formularios de autenticación para entrar a la plataforma. | Público |
| **Catálogo de Canchas** | Pantalla principal para clientes. Muestra las canchas y el buscador. | Cliente |
| **Calendario de Disponibilidad** | Vista interactiva que muestra bloques de tiempo libres y ocupados. | Cliente |
| **Mis Reservas / Historial** | Panel donde el cliente ve sus reservas pasadas/futuras y puede cancelar. | Cliente |
| **Panel de Administración** | Dashboard privado con acceso a gestión de canchas, reservas y bloqueos. | Administrador |
| **Agregar / Editar Cancha** | Formulario administrativo para actualizar los datos de las instalaciones. | Administrador |
| **Listado de Reservas** | Vista general donde el admin puede ver y cambiar el estado de cualquier reserva. | Administrador |

---

## 9. Matriz de trazabilidad

Esta matriz relaciona formalmente los Requisitos Funcionales con los Casos de Uso y las entidades del Modelo de Clases, garantizando la total cobertura funcional sin requisitos huérfanos.

| Código Req. | Descripción del Requisito | Caso de Uso Asignado | Clases Involucradas |
| :--- | :--- | :--- | :--- |
| **RF-01** | El sistema debe permitir registrar usuarios (Cliente y Administrador). | CU-01: Registrarse en el sistema | Usuario, CodigoAcceso |
| **RF-02** | El sistema debe permitir inicio de sesión seguro. | CU-02: Iniciar sesión unificado | Usuario |
| **RF-03** | Permitir consulta y edición de la información de las canchas. | CU-08: Administrar información de canchas | Cancha |
| **RF-04** | Buscar canchas filtrando por deporte, fecha, horario y precio. | CU-03: Buscar canchas con filtros | Cancha |
| **RF-05** | Mostrar interfaz de disponibilidad (calendario/horarios libres). | CU-04: Visualizar disponibilidad de horarios | Horario, Cancha |
| **RF-06** | Seleccionar bloque de tiempo y generar reserva en estado Pendiente. | CU-05: Reservar cancha | Reserva, Horario, Cancha |
| **RF-07** | Visualizar estado de reservas actuales y pasadas. | CU-07: Consultar historial de reservas | Reserva |
| **RF-08** | Permitir al cliente cancelar reservas activas con antelación mínima de 2 horas. | CU-06: Cancelar reserva | Reserva, Horario |
| **RF-09** | Administrador puede visualizar reservas, registrar reservas asistidas y actualizar estados. | CU-09: Gestionar reservas y registro asistido | Reserva, Horario |
| **RF-10** | Consultar valor estimado de reserva y liquidar con emisión de comprobante. | CU-11: Liquidar reserva y emitir comprobante | Reserva, ComprobanteLiquidacion |
| **RF-11** | Bloquear fechas/horarios por mantenimiento. | CU-10: Bloquear horarios por mantenimiento | Horario, Cancha |

### Trazabilidad gráfica

```mermaid
flowchart LR
    subgraph Sub_RF ["Requisitos Funcionales"]
        direction TB
        RF1[RF-01]
        RF2[RF-02]
        RF3[RF-03]
        RF4[RF-04]
        RF5[RF-05]
        RF6[RF-06]
        RF7[RF-07]
        RF8[RF-08]
        RF9[RF-09]
        RF10[RF-10]
        RF11[RF-11]
    end

    subgraph Sub_CU ["Casos de Uso"]
        direction TB
        CU01[CU-01]
        CU02[CU-02]
        CU03[CU-03]
        CU04[CU-04]
        CU05[CU-05]
        CU06[CU-06]
        CU07[CU-07]
        CU08[CU-08]
        CU09[CU-09]
        CU10[CU-10]
        CU11[CU-11]
    end

    subgraph Sub_Clases ["Clases del Modelo"]
        direction TB
        Usu[Usuario]
        Cod[CodigoAcceso]
        Can[Cancha]
        Hor[Horario]
        Res[Reserva]
        Comp[ComprobanteLiquidacion]
    end

    %% RF a CU
    RF1 -.-> CU01
    RF2 -.-> CU02
    RF3 -.-> CU08
    RF4 -.-> CU03
    RF5 -.-> CU04
    RF6 -.-> CU05
    RF7 -.-> CU07
    RF8 -.-> CU06
    RF9 -.-> CU09
    RF10 -.-> CU11
    RF11 -.-> CU10

    %% CU a Clases
    CU01 -.-> Usu
    CU01 -.-> Cod
    CU02 -.-> Usu
    CU03 -.-> Can
    CU04 -.-> Can
    CU04 -.-> Hor
    CU05 -.-> Res
    CU05 -.-> Hor
    CU06 -.-> Res
    CU06 -.-> Hor
    CU07 -.-> Res
    CU08 -.-> Can
    CU09 -.-> Res
    CU09 -.-> Hor
    CU10 -.-> Hor
    CU10 -.-> Can
    CU11 -.-> Res
    CU11 -.-> Comp
```

---

## 10. Auditoria y uso de ia

### Aportes individuales fase 1

| Integrantes | Cedula | Aporte individual |
| :--- | :--- | :--- |
| **Gonzalez, Walter** | 8-1027-2220 | Diseñó la arquitectura de la Fase 1 (Puntos 6 al 10): elaboración de los Casos de Uso (diagrama y descripción), diseño del Modelo de Clases, mapeo del Modelo de Navegación, estructuración de la Matriz de Trazabilidad y levantamiento de la auditoría de uso de Inteligencia Artificial para validación de procesos. |
| **Sanchez, Jose** | 8-1038-670 | Revisión de ortografía |
| **Rozette, Jose** | 8-1025-306 | Revisión de los requisitos |
| **Meneses, Alexander** | 8-1035-623 | Revisión de la estructura del documento |

### Registro de herramientas de ia utilizadas

| Herramienta | Aplicación Específica en la Fase 1 |
| :--- | :--- |
| **Gemini / Antigravity** | Utilizada como asistente de ingeniería de software para la revisión de consistencia lógica entre Requisitos Funcionales y Casos de Uso, verificación de la sintaxis de diagramas Mermaid y estructuración del documento técnico en formato Markdown para garantizar la máxima legibilidad visual y coherencia metodológica. |
| **Obsidian** | Plataforma de gestión de conocimiento y edición Markdown utilizada para el modelado estructurado de notas de requerimientos, esquemas y vinculación bidireccional entre fases del proyecto. |

---

# Fase 2: Arquitectura de Información y Diseño de Interfaz

## 1. Arquitectura de Información (AI)

### 1.1 Contenido Principal (Inventario de Contenidos)
El inventario de la plataforma se organiza en tres tipologías de contenido: informativo, funcional y mixto.

#### A. Contenido Informativo
* **Presentación del Complejo (Landing):** Identidad del centro deportivo, resumen de servicios e instalaciones, y accesos directos al catálogo.
* **Guía de Uso ("¿Cómo funciona?"):** Secuencia explicativa de cuatro pasos orientada a nuevos usuarios (exploración del catálogo, selección de cancha, consulta de disponibilidad en tiempo real y confirmación de la reserva).
* **Normativa y Equipamiento por Superficie:**
  * *Césped Sintético:* Uso exclusivo de calzado con suela tipo turf o multitaco; restricción estricta de tacos de aluminio y calzado de suela lisa.
  * *Fútbol Sala (Cemento / Tabloncillo):* Uso obligatorio de suela de goma lisa (non-marking) para preservación de la superficie y prevención de deslizamientos.
  * *Pádel / Tenis:* Calzado con suela de espiga (clay) o suela mixta; requerimientos reglamentarios para palas y raquetas.
* **Información General y Contacto:** Horarios de operación del complejo, ubicación física, canales de atención al cliente y políticas de cancelación y tolerancia horaria.

#### B. Contenido Funcional
* **Explorador Visual (Collage):** Navegación visual estructurada mediante paneles fotográficos organizados por disciplinas deportivas y tipos de instalación.
* **Buscador con Filtros Facetados y Ordenamiento:** Motor de búsqueda que opera sobre las dimensiones taxonómicas del sistema (deporte, modalidad, superficie, entorno y rango de precio).
* **Calendario de Disponibilidad:** Componente temporal dinámico que refleja los intervalos libres, ocupados o inhabilitados para cada instalación deportiva individual.
* **Módulo de Confirmación y Agendamiento de Reserva:** Interfaz para la selección de bloques horarios, revisión del resumen del turno (cancha, fecha, hora y tarifa) y registro formal de la reserva en el sistema (sin pasarelas de pago externas, conforme al alcance establecido).
* **Panel de Usuario ("Mi Cuenta"):** Interfaz para la consulta del historial de reservas del cliente (activas, completadas y canceladas) y gestión de cancelaciones para turnos vigentes.
* **Panel Administrativo (Dashboard):**
  * Gestión de Canchas (CRUD): Registro de nuevas instalaciones, actualización de especificaciones técnicas y tarifas, y desactivación lógica de canchas del catálogo público preservando la integridad del historial transaccional.
  * Control de Reservas: Supervisión global de turnos agendados y actualización de estados operativos (confirmada, completada, cancelada).
  * Reserva Asistida: Módulo para registrar reservas gestionadas por canales presenciales, telefónicos o mensajería directa, asociando los datos del solicitante al bloque horario.
  * Bloqueo Preventivo: Inhabilitación manual de fechas y horarios por mantenimiento, reparaciones o factores climáticos.

#### C. Contenido Mixto
* **Ficha de Detalle de Cancha:** Vista que integra la especificación técnica de la instalación (galería fotográfica, características de la superficie, normativa de calzado y tarifa horaria) con el componente interactivo de calendario para la consulta y selección de turnos.

---

### 1.2 Agrupaciones, Categorías y Taxonomía del Catálogo

#### A. Agrupación Temática General
1. **Exploración e Instalaciones:** Catálogo general, taxonomía deportiva y fichas individuales de cada cancha.
2. **Agendamiento y Reservas:** Consulta de disponibilidad horaria, confirmación de turno y seguimiento personal en la sección de reservas.
3. **Guía y Normativas:** Instrucciones operativas del sistema, reglamento general y especificaciones de indumentaria por cancha.
4. **Administración y Control:** Gestión de catálogo (CRUD), control de turnos, registro asistido y bloqueo de horarios.

#### B. Taxonomía Multidimensional del Catálogo
Para garantizar una categorización normalizada que facilite tanto la experiencia de filtrado del usuario como la estructuración relacional en la base de datos, el catálogo desacopla la información en cuatro dimensiones independientes:

1. **Disciplina Deportiva:** Deporte principal practicado en la instalación (Fútbol, Pádel, Baloncesto, Tenis).
2. **Modalidad y Formato:** Configuración de juego admitida por las dimensiones de la cancha:
   * *Fútbol:* Fútbol 5, Fútbol 7, Fútbol 9.
   * *Pádel / Tenis:* Individual, Dobles.
   * *Baloncesto:* Media cancha (3x3), Cancha completa (5x5).
3. **Tipo de Superficie:** Material constructivo del suelo, determinante para la normativa de calzado:
   * Césped sintético (fibras con relleno de caucho/arena).
   * Tabloncillo / Parqué de madera tratada.
   * Concreto pulido / Cemento sintético.
   * Arcilla / Tierra batida.
4. **Entorno de la Instalación (Cubierta):** Condición estructural frente al clima:
   * Techada / Cubierta cerrada.
   * Al aire libre / Exterior.

Cada cancha física representa una instancia concreta que combina estas cuatro dimensiones, vinculando un sector específico dentro del complejo deportivo y una tarifa horaria base.

---

### 1.3 Jerarquía de la Información y Arquitectura de Pantallas

La arquitectura de información distribuye el sistema en tres niveles de profundidad, diferenciando páginas independientes de componentes modales:

* **Nivel 1 (Acceso Global - Páginas Independientes):**
  * Inicio (Landing page), Catálogo / Explorar Canchas, ¿Cómo Funciona?, Normas de Cancha, e Iniciar Sesión / Registro.
* **Nivel 2 (Vistas de Contenido y Gestión - Páginas Independientes):**
  * *Vistas de Cliente:* Resultados del Buscador con Filtros, Ficha de Detalle de Cancha y Mis Reservas (Historial).
  * *Vistas de Administrador:* Dashboard de Gestión, Formulario para Agregar / Editar Cancha y Listado General de Reservas.
* **Nivel 3 (Componentes de Interacción Contextual - Modales en Capa de Interfaz):**
  * Los modales no constituyen nodos de navegación ni poseen URLs independientes; operan como capas sobrepuestas en las pantallas de Nivel 2:
    * **Modal de Confirmación de Reserva:** Disparado desde la Ficha de Detalle de Cancha al seleccionar un bloque horario; procesa el agendamiento sin abandonar la vista del calendario.
    * **Modal de Cancelación:** Disparado desde Mis Reservas; solicita validación explícita antes de liberar el registro.
    * **Modal de Bloqueo de Horarios:** Disparado desde Gestión de Canchas; define intervalos de inhabilitación por mantenimiento.
    * **Modal de Cambio de Estado:** Disparado desde el Listado de Reservas; actualiza el ciclo de vida del turno.
    * **Modal de Reserva Asistida:** Disparado desde el Listado de Reservas; permite al personal administrativo agendar turnos presenciales o telefónicos.

---

### 1.4 Sistema de Etiquetas, Accesibilidad y Disponibilidad Dinámica

#### A. Estandarización de Etiquetas

| Etiqueta en Interfaz | Propósito / Acción | Tipo de Elemento | Nivel de Acceso |
| :--- | :--- | :--- | :--- |
| **Explorar Canchas** | Acceso al catálogo y cuadrícula visual de instalaciones. | Menú / Navegación | Público |
| **¿Cómo Funciona?** | Guía de cuatro pasos para el proceso de reserva. | Enlace Informativo | Público |
| **Normas de Cancha** | Requisitos de calzado y reglamento por tipo de superficie. | Enlace Informativo | Público |
| **Consultar Disponibilidad** | Visualización de la matriz horaria por fecha. | Sección Funcional | Público |
| **Reservar Horario** | Acción principal para confirmar el turno seleccionado. | Botón de Acción | Cliente autenticado |
| **Mis Reservas** | Consulta de turnos vigentes e historial de reservas. | Menú de Cuenta | Cliente |
| **Panel de Control** | Acceso al módulo de administración operativa. | Menú Privado | Administrador |
| **Bloquear Horarios** | Acción para inhabilitar intervalos por mantenimiento. | Botón Funcional | Administrador |

#### B. Accesibilidad Web (WCAG 2.1 Nivel AA) y Diseño Responsivo
En cumplimiento del requisito RNF-01 (Usabilidad) y del estándar de accesibilidad WCAG 2.1 Nivel AA, la interfaz adopta las siguientes especificaciones técnicas:

1. **Contraste Cromático:** Todos los elementos textuales e indicadores de interfaz mantienen un contraste mínimo de 4.5:1 respecto a su fondo para texto estándar, y de 3:1 para componentes gráficos interactivos.
2. **Identificación Multimodal de Estados:** La disponibilidad horaria no se transmite únicamente mediante color, combinando tres señales simultáneas:
   * *Intervalo Libre:* Fondo verde accesible (#2E7D32), texto legible "Libre" e icono de confirmación con atributo `aria-label="Horario disponible"`.
   * *Intervalo Ocupado:* Fondo gris neutro (#616161), texto "Ocupado", icono de bloqueo y atributo accesible `aria-disabled="true"`.
   * *Intervalo en Mantenimiento:* Fondo amarillo advertencia (#F57F17) con trama rayada de alto contraste, texto "Mantenimiento" e icono de alerta.
3. **Navegación Asistida por Teclado:** Toda la matriz de turnos y formularios admiten navegación secuencial lógica mediante la tecla Tab, con indicadores visuales de foco activos (`:focus-visible`).
4. **Adaptabilidad del Calendario en Dispositivos Móviles:**
   * En resoluciones de escritorio (> 768px), el calendario se renderiza como una cuadrícula matricial de bloques horarios.
   * En pantallas móviles (<= 768px), la vista colapsa a un carrusel selector de fecha superior combinado con un listado vertical de tarjetas horarias.

#### C. Dinámica de Disponibilidad y Control de Concurrencia
La disponibilidad de los horarios opera bajo un modelo de sincronización y validación transaccional:
1. **Consulta Asíncrona:** La carga de disponibilidad en la ficha de cancha se ejecuta mediante peticiones asíncronas al servidor (AJAX/Fetch) al seleccionar la fecha deseada.
2. **Validación Transaccional en Dos Pasos:** Al presionar "Reservar Horario", el backend ejecuta una verificación de disponibilidad inmediata en la base de datos justo antes de asentar el registro (`COMMIT`).
3. **Manejo de Condiciones de Carrera:** Si dos clientes intentan reservar el mismo intervalo simultáneamente, la transacción que se procese primero bloquea el registro; la segunda es rechazada de forma controlada por el backend, emitiendo un mensaje descriptivo conforme al flujo alterno de CU-05.

---

### 1.5 Mecanismos de Acceso y Reglas de Autenticación

#### A. Regla Operativa de Acceso: Refinamiento de Experiencia de Usuario (UX)
El sistema implementa un modelo de acceso y navegación estructurado para optimizar la experiencia de usuario (UX):
1. **Navegación y Consulta Pública (Visitante):** Cualquier usuario puede explorar el catálogo, utilizar el buscador facetado y consultar la disponibilidad horaria sin registro previo.
2. **Intercepción de Autenticación en el Agendamiento:** Al pulsar "Reservar Horario", si no existe una sesión activa, el sistema intercepta el flujo y redirige al formulario de acceso, reteniendo en memoria los parámetros de la reserva para reanudar el proceso tras autenticarse (conforme a CU-05 y RF-06).

#### B. Mecanismos de Búsqueda y Navegación
1. **Navegación Jerárquica Visual:** Acceso estructurado a través del collage fotográfico principal.
2. **Búsqueda Facetada:** Filtrado cruzado por disciplina, modalidad, superficie, entorno y precio, con opciones de ordenamiento por tarifa y sector.
3. **Navegación Global (Barra Superior):** Menú persistente con enlaces directos a las páginas de Nivel 1 y control de sesión.
4. **Navegación Contextual:** Menú lateral operativo en el panel administrativo y pestañas organizadoras dentro de la ficha de detalle de cancha.
5. **Navegación Suplementaria:** Migas de pan estructurales (ejemplo: Inicio > Fútbol > Césped Sintético > Cancha 1) y pie de página institucional.

---

## 2. Sitemap (Mapa del Sitio)

### 2.1 Estructura Jerárquica del Sitio (Diagrama Mermaid)

El siguiente diagrama modela la estructura de páginas y rutas navegables del sistema (los componentes modales se integran en la capa de interfaz descrita en la sección 1.3):

```mermaid
graph TD
    %% Nivel 0: Raiz Publica
    Home["1.0 Inicio (Landing Page)"]

    %% Nivel 1: Secciones Publicas Principales
    Explorar["2.0 Explorar Canchas"]
    ComoFunciona["3.0 Como Funciona"]
    Normas["4.0 Normas y Calzado"]
    Contacto["5.0 Contacto y Ubicacion"]
    Auth["6.0 Autenticacion"]

    %% Conexiones desde Raiz Publica
    Home --> Explorar
    Home --> ComoFunciona
    Home --> Normas
    Home --> Contacto
    Home --> Auth

    %% Nivel 2: Ramas de Exploracion
    Collage["2.1 Collage por Deportes"]
    Buscador["2.2 Buscador con Filtros"]
    FichaCancha["2.3 Ficha de Detalle de Cancha"]

    Explorar --> Collage
    Explorar --> Buscador
    Explorar --> FichaCancha

    %% Nivel 2: Ramas de Autenticacion
    Login["6.1 Iniciar Sesion"]
    Registro["6.2 Registrarse"]

    Auth --> Login
    Auth --> Registro

    %% Nivel 2: Vistas Privadas Condicionadas a Sesion
    MiCuenta["7.0 Mi Cuenta (Cliente - Requiere Sesion)"]
    AdminPanel["8.0 Panel de Control (Admin - Requiere Sesion)"]

    Auth -.->|Sesion Valida: Cliente| MiCuenta
    Auth -.->|Sesion Valida: Administrador| AdminPanel

    %% Nivel 2: Subpaginas de Mi Cuenta
    MisReservas["7.1 Mis Reservas (Historial)"]
    MiCuenta --> MisReservas

    %% Nivel 2: Subpaginas de Administracion
    CrudCanchas["8.1 Gestion de Canchas"]
    ListadoReservas["8.2 Listado de Reservas"]
    FormCancha["8.1.1 Formulario Agregar / Editar Cancha"]

    AdminPanel --> CrudCanchas
    AdminPanel --> ListadoReservas
    CrudCanchas --> FormCancha

    %% Estilos Graficos
    style Home fill:#2C3E50,stroke:#1A252F,color:#fff
    style Explorar fill:#34495E,stroke:#2C3E50,color:#fff
    style ComoFunciona fill:#2E4053,stroke:#1C2833,color:#fff
    style Normas fill:#2E4053,stroke:#1C2833,color:#fff
    style Contacto fill:#2E4053,stroke:#1C2833,color:#fff
    style Auth fill:#7F8C8D,stroke:#616A6B,color:#fff
    style MiCuenta fill:#1F618D,stroke:#154360,color:#fff
    style AdminPanel fill:#78281F,stroke:#511B15,color:#fff
```

---

### 2.2 Desglose Estructurado de Páginas y Secciones

#### Nivel 0: Raíz Pública
* **1.0 Inicio (Landing Page):** Página principal. Presenta la identidad institucional, acceso al collage deportivo, llamadas a la acción para agendamiento y menús globales.

#### Nivel 1: Secciones Públicas y Catálogo
* **2.0 Explorar Canchas:** Sección contenedora del catálogo general de instalaciones deportivas.
* **3.0 ¿Cómo Funciona?:** Guía conceptual explicativa del proceso de reserva de canchas.
* **4.0 Normas y Calzado:** Especificaciones reglamentarias de indumentaria y calzado admitido según la superficie.
* **5.0 Contacto y Ubicación:** Mapa físico, canales de atención al cliente y horarios generales de funcionamiento.
* **6.0 Autenticación:** Módulo de control de acceso y registro de cuentas de usuario.

#### Nivel 2: Subpáginas y Vistas de Gestión
* **2.1 Collage por Deportes:** Vista de navegación visual guiada que desglosa disciplinas e instalaciones.
* **2.2 Buscador con Filtros:** Vista de catálogo con interfaz de búsqueda facetada por dimensiones técnicas y tarifarias.
* **2.3 Ficha de Detalle de Cancha:** Página individual que integra las especificaciones de la cancha, fotos, requisitos de calzado y el componente interactivo de calendario de disponibilidad.
* **6.1 Iniciar Sesión:** Formulario de autenticación mediante correo y contraseña, con redirección condicionada por rol.
* **6.2 Registrarse:** Formulario de alta para clientes nuevos, con campo para código de acceso de empleados.
* **7.1 Mis Reservas:** Interfaz de control del cliente que lista sus turnos activos e histórico de reservas pasadas.
* **8.1 Gestión de Canchas:** Tabla de inventario de instalaciones con opciones operativas de edición y desactivación.
  * **8.1.1 Formulario Agregar / Editar Cancha:** Página independiente para la captura y actualización de datos técnicos, fotos y tarifas de cada instalación.
* **8.2 Listado de Reservas:** Vista cronológica y tabular de todas las reservas registradas en el sistema, permitiendo filtrado y supervisión operativa.

---

### 2.3 Matriz de Accesibilidad por Tipo de Usuario

| Código | Página / Sección | Visitante (Público) | Cliente Autenticado | Administrador |
| :--- | :--- | :---: | :---: | :---: |
| **1.0** | Inicio | Permitido | Permitido | Permitido |
| **2.0** | Explorar Canchas (Collage / Buscador) | Permitido | Permitido | Permitido |
| **2.3** | Ficha de Detalle de Cancha (con Calendario) | Permitido (Consulta) | Permitido (Consulta) | Permitido (Consulta) |
| **3.0** | ¿Cómo Funciona? | Permitido | Permitido | Permitido |
| **4.0** | Normas y Calzado | Permitido | Permitido | Permitido |
| **5.0** | Contacto y Ubicación | Permitido | Permitido | Permitido |
| **6.0** | Autenticación (Login / Registro) | Permitido | Redirige a Perfil | Redirige a Panel |
| **7.0** | Mi Cuenta (7.1 Mis Reservas) | Restringido | Permitido | Restringido |
| **8.0** | Panel de Control (8.1 Canchas / 8.2 Reservas) | Restringido | Restringido | Permitido |
| **8.1.1** | Formulario Agregar / Editar Cancha | Restringido | Restringido | Permitido |

---

## 3. Modelo de Navegación Refinado

### 3.1 Diagrama de Navegación

El siguiente diagrama modela las rutas disponibles, transiciones entre vistas y accesos según el rol del usuario:

```mermaid
flowchart TD
    Home["1.0 Inicio"]
    Info["3.0 / 4.0 / 5.0\nInfo / Normas / Contacto"]
    Catalogo["2.0 Catálogo / Explorar"]
    Buscador["2.2 Buscador y Filtros"]
    Ficha["2.3 Ficha de Cancha\n(con Calendario)"]
    Login["6.1 Iniciar Sesión"]
    Registro["6.2 Registrarse"]
    MisReservas["7.1 Mis Reservas\n(Cliente)"]
    AdminDash["8.0 Panel de Control\n(Admin)"]
    AdminCanchas["8.1 Gestión Canchas"]
    AdminForm["8.1.1 Formulario Cancha"]
    AdminReservas["8.2 Listado Reservas"]

    Home -->|Menú Global| Info
    Home -->|Menú Global / CTA| Catalogo
    Home -->|Botón Acceso| Login
    Home -->|Botón Registro| Registro
    Home -->|Menú Global| Buscador

    Catalogo -->|Barra de búsqueda / Filtros| Buscador
    Buscador -->|Migas de pan| Catalogo
    Catalogo -->|Seleccionar Cancha| Ficha
    Buscador -->|Seleccionar Cancha| Ficha
    Ficha -->|Migas de pan| Catalogo

    Ficha -->|Sin sesión| Login
    Login -->|Retoma reserva| Ficha
    Login -->|No tiene cuenta| Registro
    Registro -->|Cuenta creada| Login

    Login -->|Rol: Cliente| Catalogo
    Login -->|Rol: Administrador| AdminDash

    Ficha -->|Autenticado: confirmar turno| MisReservas
    Login -->|Venía de Mis Reservas| MisReservas
    MisReservas -->|Menú de usuario| Catalogo
    MisReservas -->|Menú Global| Home
    MisReservas -->|Cerrar sesión| Home

    AdminDash -->|Sidebar| AdminCanchas
    AdminDash -->|Sidebar| AdminReservas
    AdminDash -->|Enlace Superior| Home
    AdminDash -->|Cerrar sesión| Home

    AdminCanchas -->|Botón Agregar/Editar| AdminForm
    AdminForm -->|Guardar / Cancelar| AdminCanchas
    AdminCanchas -->|Sidebar| AdminReservas
    AdminReservas -->|Sidebar| AdminCanchas
```

---

### 3.2 Pantallas del Sistema

| Código | Pantalla | Descripción | Acceso |
| :--- | :--- | :--- | :--- |
| **1.0** | Inicio | Página de entrada con llamada a la acción, collage deportivo y acceso a registro e inicio de sesión. | Público |
| **2.0** | Catálogo / Explorar | Listado de canchas disponibles. | Público |
| **2.2** | Buscador y Filtros | Barra de búsqueda y panel lateral de filtros (deporte, modalidad, superficie, entorno y precio). | Público |
| **2.3** | Ficha de Cancha | Detalle de la cancha con calendario de disponibilidad. Para reservar se requiere sesión. | Público (reservar: Cliente) |
| **3.0 / 4.0 / 5.0** | Info / Normas / Contacto | Páginas informativas del complejo. | Público |
| **6.1** | Iniciar Sesión | Autenticación; redirige según el rol. | Público |
| **6.2** | Registrarse | Creación de cuenta de cliente (o de administrador con código de acceso). | Público |
| **7.1** | Mis Reservas | Historial de reservas y cancelación. | Cliente |
| **8.0** | Panel de Control | Inicio del área administrativa. | Administrador |
| **8.1** | Gestión de Canchas | Tabla del catálogo, alta, edición, desactivación y bloqueo de horarios. | Administrador |
| **8.1.1** | Formulario de Cancha | Formulario para agregar o editar una cancha. | Administrador |
| **8.2** | Listado de Reservas | Todas las reservas del complejo, cambio de estado y reserva asistida. | Administrador |

---

### 3.3 Navegación Principal y Secundaria por Rol

| Elemento | Visitante | Cliente | Administrador |
| :--- | :--- | :--- | :--- |
| **Navegación principal (menú global)** | Inicio, Catálogo, Info / Normas / Contacto | Inicio, Catálogo, Info / Normas / Contacto | Enlace superior a Inicio |
| **Menú de usuario** | Botones Acceso (6.1) y Registro (6.2) | Mis Reservas (7.1) y Cerrar sesión | Cerrar sesión |
| **Navegación secundaria** | Filtros y buscador (2.2); calendario de la Ficha (2.3) | Filtros y buscador (2.2); calendario; botón Cancelar reserva en 7.1 | Sidebar: Gestión de Canchas (8.1) y Listado de Reservas (8.2) |
| **Migas de pan** | Inicio > Catálogo > Ficha | Inicio > Catálogo > Ficha | Panel > Gestión de Canchas > Formulario |
| **Acciones contextuales (modales)** | Intercepción de sesión al reservar | Confirmación de turno; cancelación de reserva | Bloqueo de horarios; reserva asistida |
| **Pantallas restringidas** | 7.1 y 8.x redirigen a Iniciar Sesión | 8.x no accesible | 7.1 no aplica |

---

## 4. Flujos de Navegación

Cada flujo modela el recorrido de una tarea crítica en 5 a 7 pasos principales, con nodos de decisión (rombos) para la sesión activa, los campos obligatorios y la colisión de reservas.

### Flujo 1: Búsqueda, Selección y Agendamiento de una Cancha

| Campo | Descripción |
| :--- | :--- |
| **Actor** | Cliente (o visitante) |
| **Objetivo** | Buscar una cancha, elegir un horario libre y confirmar la reserva. |
| **Precondición** | El usuario está en el Catálogo (2.0). Si es visitante, el sistema lo intercepta antes de confirmar. |
| **Resultado esperado** | La reserva queda registrada, el horario pasa a Ocupado y se muestra Mis Reservas (7.1). |
| **Excepción principal** | Si otro usuario confirmó el mismo bloque antes, se muestra «Este horario ya no está disponible. Seleccione otro.» y se actualiza el calendario. |

```mermaid
flowchart TD
    P1["1. Buscar y filtrar canchas\nCatálogo 2.0 / Buscador 2.2"] --> P2["2. Abrir Ficha de Cancha 2.3\ny consultar el calendario"]
    P2 --> P3["3. Elegir un horario Libre y\npulsar Reservar Horario"]
    P3 --> D1{"¿Hay sesión\nactiva?"}
    
    D1 -->|No: visitante| P4["4. Intercepción: Iniciar Sesión 6.1 o\nRegistro 6.2 (reserva retenida en memoria)"]
    D1 -->|Sí: cliente| P5["5. Modal de Confirmación: resumen\n(cancha, fecha, hora, precio) y Confirmar"]
    
    P4 --> D2{"¿Tiene\ncuenta?"}
    D2 -->|No: Registro 6.2| P4a["Registro 6.2: completar nombre, correo,\nteléfono y contraseña. Cuenta creada,\nvuelve a Iniciar Sesión 6.1"]
    D2 -->|Sí: Iniciar Sesión 6.1| D3{"¿Credenciales\nválidas?"}
    
    P4a --> D4{"¿Campos\ncompletos?"}
    D4 -->|No| E1["Error de campos requeridos\nSe conservan los datos escritos\n-> vuelve al paso 4"]
    D4 -->|Sí| D3
    
    D3 -->|No| E2["Correo o contraseña incorrectos\nSe conserva el correo\n-> vuelve al paso 4"]
    D3 -->|Sí: regresa a 2.3| P5
    
    P5 --> P6["6. El sistema verifica la disponibilidad\njusto antes de guardar la reserva"]
    P6 --> D5{"¿El horario\nsigue libre?"}
    
    D5 -->|No: otro usuario confirmó antes| E3["Este horario ya no está disponible.\nSeleccione otro.\n-> calendario actualizado (paso 2)"]
    D5 -->|Sí| P7["7. Reserva registrada y confirmada\nSe muestra Mis Reservas 7.1"]
```

---

### Flujo 2: Consulta de Historial y Cancelación de una Reserva Vigente

| Campo | Descripción |
| :--- | :--- |
| **Actor** | Cliente |
| **Objetivo** | Revisar el historial de reservas y cancelar una reserva vigente. |
| **Precondición** | El cliente tiene sesión activa (si es visitante, se redirige a Iniciar Sesión 6.1 y regresa a Mis Reservas) y accede desde el menú de usuario. |
| **Resultado esperado** | La reserva cambia a Cancelada, el horario queda libre y la tarjeta se actualiza en Mis Reservas (7.1). |
| **Excepción principal** | Si el cliente no tiene reservas se muestra un mensaje informativo; si no confirma la cancelación, la reserva se mantiene sin cambios. |

```mermaid
flowchart TD
    P1["1. Acceder a Mis Reservas 7.1\ndesde el menú de usuario"] --> D1{"¿Hay sesión de\nCliente activa?"}
    D1 -->|No: visitante| E1["Visitante: redirige a Iniciar Sesión 6.1\n-> regresa a Mis Reservas al autenticarse"]
    D1 -->|Sí: cliente| P2["2. Consultar el historial: reservas\nconfirmadas, completadas y canceladas"]
    P2 --> D2{"¿Tiene reservas\nregistradas?"}
    D2 -->|No| E2["Aún no tienes reservas registradas\nFin de la consulta"]
    D2 -->|Sí| P3["3. Seleccionar la reserva vigente\ny pulsar Cancelar Reserva"]
    P3 --> P4["4. Modal de Cancelación: ¿Está seguro de\nque desea cancelar esta reserva?"]
    P4 --> D3{"¿Confirma la\ncancelación?"}
    D3 -->|No| E3["La reserva se mantiene sin cambios\n-> vuelve a Mis Reservas 7.1"]
    D3 -->|Sí| P5["5. El sistema cambia el estado a\nCancelada y libera el horario"]
    P5 --> P6["6. Mis Reservas 7.1 actualizada:\nla tarjeta pasa a estado Cancelada"]
```

---

### Flujo 3: Registro de una Nueva Cancha en el Catálogo (CRUD)

| Campo | Descripción |
| :--- | :--- |
| **Actor** | Administrador |
| **Objetivo** | Agregar una nueva cancha con su información técnica y tarifa. |
| **Precondición** | El administrador inició sesión y está en el Panel de Control (8.0). |
| **Resultado esperado** | La nueva cancha aparece en la tabla de Gestión de Canchas (8.1) y en el catálogo público. |
| **Excepción principal** | Si faltan campos obligatorios, se muestra el error sin borrar lo ya escrito. |

```mermaid
flowchart TD
    P1["1. Ingresar al Panel de\nControl 8.0 (Administrador)"] --> P2["2. Sidebar: abrir\nGestión de Canchas 8.1"]
    P2 --> P3["3. Pulsar + Nueva Cancha\n(abre el formulario 8.1.1)"]
    P3 --> P4["4. Completar los datos de la cancha\n(información técnica y tarifa)"]
    P4 --> D1{"¿Guardar o\nCancelar?"}
    D1 -->|Cancelar| E1["Retorno a 8.1 sin cambios"]
    D1 -->|Guardar| P5["5. Pulsar Guardar"]
    P5 --> D2{"¿Campos obligatorios\ncompletos?"}
    D2 -->|No| E2["Complete todos los campos requeridos\nSe conserva lo ya escrito\n-> vuelve al paso 4"]
    D2 -->|Sí| P6["6. El sistema valida y\nactualiza la base de datos"]
    P6 --> P7["7. Retorno a 8.1: la nueva cancha aparece\nen la tabla y en el catálogo público"]
```

---

### Flujo 4: Bloqueo Manual de Horarios por Mantenimiento o Lluvia

| Campo | Descripción |
| :--- | :--- |
| **Actor** | Administrador |
| **Objetivo** | Bloquear un rango de fechas y horas de una cancha por mantenimiento o lluvia. |
| **Precondición** | El administrador inició sesión y está en Gestión de Canchas (8.1). |
| **Resultado esperado** | Los bloques quedan no disponibles y el calendario público (2.3) los muestra como Mantenimiento. |
| **Excepción principal** | Si hay reservas activas en el rango, no se bloquea y se pide resolverlas primero en el Listado de Reservas (8.2). |

```mermaid
flowchart TD
    P1["1. Ingresar al Panel de\nControl 8.0 (Administrador)"] --> P2["2. Sidebar: abrir\nGestión de Canchas 8.1"]
    P2 --> P3["3. Elegir la cancha y pulsar\nBloquear Horarios"]
    P3 --> P4["4. Modal de Bloqueo: definir el motivo\n(mantenimiento o lluvia) y el rango de fechas y horas"]
    P4 --> P5["5. Pulsar Confirmar bloqueo"]
    P5 --> D1{"¿Campos obligatorios\ncompletos?"}
    D1 -->|No| E1["Mensaje de campos requeridos\nSe conserva lo ya escrito\n-> vuelve al paso 4"]
    D1 -->|Sí| D2{"¿Hay reservas activas\nen el rango?"}
    D2 -->|Sí| E2["Advertencia: hay reservas activas en el rango.\nNo se bloquea. Resolverlas en Listado de\nReservas 8.2 (CU-09) -> y reintentar (paso 3)"]
    D2 -->|No| P6["6. El sistema marca los bloques como\nno disponibles (estado Mantenimiento)"]
    P6 --> P7["7. El calendario público 2.3 muestra\nMantenimiento: no se puede reservar"]
```

---

### Flujo 5: Registro de una Reserva Asistida (Atención Presencial o Telefónica)

| Campo | Descripción |
| :--- | :--- |
| **Actor** | Administrador |
| **Objetivo** | Registrar una reserva a nombre de un solicitante que llegó o llamó al complejo. |
| **Precondición** | El administrador inició sesión y está en el Listado de Reservas (8.2). |
| **Resultado esperado** | La reserva queda registrada, el horario pasa a Ocupado y aparece en el Listado de Reservas (8.2). |
| **Excepción principal** | Si faltan campos obligatorios se conserva lo escrito; si el bloque ya fue reservado, se pide elegir otro. |

```mermaid
flowchart TD
    P1["1. Ingresar al Panel de\nControl 8.0 (Administrador)"] --> P2["2. Sidebar: abrir\nListado de Reservas 8.2"]
    P2 --> P3["3. Pulsar + Reserva Asistida\n(abre el modal)"]
    P3 --> P4["4. Registrar los datos del solicitante\ny el canal (presencial o telefónico)"]
    P4 --> P5["5. Elegir cancha, fecha y\nbloque horario libre"]
    P5 --> D1{"¿Campos obligatorios\ncompletos?"}
    D1 -->|No| E1["Mensaje de campos requeridos\nSe conserva lo ya escrito\n-> vuelve al paso 4"]
    D1 -->|Sí| P6["6. Pulsar Confirmar: el sistema verifica\nla disponibilidad antes de guardar"]
    P6 --> D2{"¿El horario\nsigue libre?"}
    D2 -->|No: otro bloque ya fue reservado| E2["Este horario ya no está disponible.\nSeleccione otro.\n-> vuelve al paso 5"]
    D2 -->|Sí| P7["7. Reserva registrada: el horario pasa\na Ocupado y aparece en 8.2"]
```

---

# Auditoría y Uso de la IA

## Tabla 1. Auditoría y Uso de la IA - Fase 1 (Mini Avance 1)

| Sección | Integrante(s) | Herramienta y Link al prompt utilizado | Aporte de la IA | Aporte Intelectual del equipo |
| :--- | :--- | :--- | :--- | :--- |
| Repositorio, Despliegue y Descripción del Proyecto | Gonzalez, Walter | Antigravity / Gemini — [Ver prompts en Auditoria/prompts.md](./Auditoria/prompts.md) | Asistió en la estructuración del README en formato Markdown y corrección de coherencia en la redacción inicial. | Configuración del repositorio en GitHub, despliegue en GitHub Pages, y formulación del problema, propósito, objetivo general y alcance del sistema. |
| Identificación de Usuarios | Sanchez, Jose | Ninguna | Ninguno | Análisis y caracterización de los perfiles de Cliente y Administrador, identificando sus necesidades y funciones clave en el sistema. |
| Requisitos Funcionales | Rozette, Jose | Ninguna | Ninguno | Definición técnica y tabulación completa de los requisitos funcionales del sistema (RF-01 a RF-09). |
| Requisitos No Funcionales y Escenarios de Uso | Meneses, Alexander | Ninguna | Ninguno | Formulación de los requisitos no funcionales (RNF-01 a RNF-08) y desarrollo estructurado de los escenarios de uso paso a paso. |

---

## Tabla 2. Auditoría y Uso de la IA - Fase 1 (Parte 2)

| Sección | Integrante(s) | Herramienta y Link al prompt utilizado | Aporte de la IA | Aporte Intelectual del equipo |
| :--- | :--- | :--- | :--- | :--- |
| Casos de Uso, Modelo de Clases, Navegación y Trazabilidad | Gonzalez, Walter | Antigravity / Gemini — [Ver prompts en Auditoria/prompts.md](./Auditoria/prompts.md) | Asistió en la estructuración técnica del README y en la revisión de coherencia de los modelos. | Diseño de casos de uso (flujo principal y excepciones), modelado de clases del dominio, arquitectura de navegación y matriz de trazabilidad. |
| Revisión de Ortografía y Redacción | Sanchez, Jose | Ninguna | Ninguno | Revisión de ortografía, estilo y redacción técnica de los entregables de la parte 2. |
| Validación de Requisitos | Rozette, Jose | Ninguna | Ninguno | Verificación cruzada para asegurar la cobertura de todos los requisitos funcionales en las clases y casos de uso. |
| Control de Estructura | Meneses, Alexander | Ninguna | Ninguno | Inspección de la estructura documental conforme a los criterios de evaluación de la cátedra. |

---

## Tabla 3. Auditoría y Uso de la IA - Fase 2 (Avance Actual)

| Sección | Integrante(s) | Herramienta y Link al prompt utilizado | Aporte de la IA | Aporte Intelectual del equipo |
| :--- | :--- | :--- | :--- | :--- |
| Arquitectura de Información y Sitemap | Gonzalez, Walter | Antigravity / Gemini — [Ver prompts en Auditoria/prompts.md](./Auditoria/prompts.md) | Asistió en la maquetación del documento en formato Markdown y en la revisión de coherencia técnica entre las especificaciones de arquitectura y navegación. | Definición de las reglas de negocio, taxonomía multidimensional del catálogo, especificaciones de accesibilidad WCAG 2.1 AA, lógica de concurrencia y diseño jerárquico del sitemap. |
| Modelo de Navegación Refinado y Flujos de Navegación | Sanchez, Jose | Gemini — [Ver prompts en Auditoria/prompts.md](./Auditoria/prompts.md) | Asistió en la estructuración de los diagramas de flujo de tareas críticas y en la depuración de pasos redundantes e inconsistencias lógicas. | Elaboración del diagrama de navegación general, estructuración de las matrices de pantallas y roles, y modelado detallado de los cinco flujos de tareas críticas con manejo de decisiones, intercepción de sesión y excepciones. |
| Wireframes | Rozette, Jose | En desarrollo | En desarrollo | Asignado para el diseño estructural de las pantallas principales en media fidelidad. |
| Prototipo de Alta Fidelidad | Meneses, Alexander | En desarrollo | En desarrollo | Asignado para la construcción visual interactiva y componentes en Figma. |
