# Avance 1: Sistema Web para Reserva de Canchas e Instalaciones Deportivas

## 1. Descripción del proyecto
*   **Nombre del Proyecto:** Sistema web para reserva de canchas e instalaciones deportivas
*   **Problema o necesidad:** La dificultad y pérdida de tiempo que enfrentan los usuarios al intentar encontrar canchas disponibles debido a la falta de información centralizada. Asimismo, la ineficiencia de los administradores de los complejos deportivos al llevar el control de reservas, horarios y cancelaciones de manera manual.
*   **Propósito:** Proporcionar un sistema digitalizado y centralizar la información respecto a la reserva de canchas.
*   **Objetivo general:** Diseñar e implementar una plataforma web centralizada que mejore la experiencia de los usuarios en la búsqueda y reserva de canchas deportivas, garantizando el acceso a información actualizada y detallada sobre las instalaciones en todo momento.
*   **Alcance:** El proyecto abarcará el diseño y desarrollo de una aplicación web responsiva. Incluirá un catálogo digital de instalaciones deportivas con sus respectivos detalles (costos, ubicación y condiciones). Contará con un módulo para clientes (orientado a la consulta de disponibilidad y generación de reservas) y un módulo administrativo (para la gestión de canchas y control de las reservas agendadas).
*   **Principales funcionalidades:**
    *   Registro y autenticación de usuarios (perfil cliente y perfil administrador).
    *   Buscador de canchas con filtros por tipo de deporte y disponibilidad de fechas/horarios.
    *   Calendario interactivo para visualizar horarios libres y ocupados en tiempo real.
    *   Sistema de generación, confirmación y cancelación de reservas.
    *   Panel de administración para agregar/editar la información de las canchas y gestionar el estado de las reservas.

## 2. Identificación de usuarios

### Cliente
*   **Características:** Personas de diversas edades interesadas en practicar deportes o realizar actividades físicas. Por lo general, disponen de poco tiempo y buscan soluciones rápidas y convenientes.
*   **Necesidades:**
    *   Encontrar rápidamente una cancha disponible que se ajuste a su deporte, horario y presupuesto.
    *   Conocer las características exactas de la instalación (ubicación, si es techada, tipo de piso, precio) antes de reservar.
    *   Realizar una reserva de forma inmediata sin tener que hacer llamadas telefónicas, esperar confirmaciones por WhatsApp o ir presencialmente al lugar.
*   **Funciones principales en el sistema:**
    *   Registrarse e iniciar sesión.
    *   Buscar y filtrar canchas (por deporte, fecha y hora).
    *   Visualizar el calendario interactivo de disponibilidad.
    *   Realizar la reserva de un horario específico.
    *   Cancelar una reserva previamente hecha.
    *   Ver su historial de reservas (pasadas y próximas).

### Administrador
*   **Características:** Personal empleado por el complejo deportivo (recepcionistas, gerentes o dueños). Tienen conocimientos básicos o intermedios en el uso de sistemas informáticos y son los responsables directos de la atención al público, el cobro y el mantenimiento de las instalaciones.
*   **Necesidades:**
    *   Mantener un control organizado y centralizado de todas las reservas del día para evitar el "choque" o cruce de horarios (dos personas reservando la misma cancha).
    *   Poder bloquear horarios si una cancha entra en reparación o mantenimiento.
    *   Tener acceso a los datos de contacto del cliente en caso de que ocurra algún inconveniente con la reserva.
*   **Funciones principales en el sistema:**
    *   Iniciar sesión en un panel de control privado (Dashboard).
    *   Gestionar el catálogo de instalaciones: Agregar nuevas canchas, editar su información (precios, fotos, estado) o eliminarlas.
    *   Visualizar un listado completo o calendario con todas las reservas agendadas por los clientes.
    *   Cambiar el estado de las reservas (ej. confirmada, cancelada, completada).
    *   Bloquear manualmente horarios de las canchas por motivos de cierre o mantenimiento.

## 3. Requisitos funcionales

| Código | Módulo | Descripción del Requisito | Usuario |
| :--- | :--- | :--- | :--- |
| **RF-01** | Seguridad | El sistema debe permitir a los usuarios nuevos registrarse creando una cuenta con sus datos personales, asignando el rol de 'Cliente' por defecto, o el rol de 'Administrador' mediante el ingreso de un código de acceso especial. | Ambos |
| **RF-02** | Seguridad | El sistema debe permitir el inicio de sesión seguro utilizando el correo electrónico y contraseña. | Ambos |
| **RF-03** | Catálogo | El sistema debe permitir agregar, editar, visualizar y eliminar (CRUD) la información de las canchas deportivas, incluyendo nombre, deporte, precio, ubicación, condiciones y estado. | Administrador |
| **RF-04** | Búsqueda | El sistema debe permitir buscar canchas filtrando los resultados por tipo de deporte, fecha, horario y precio. | Cliente |
| **RF-05** | Reservas | El sistema debe mostrar una interfaz (calendario o bloques de tiempo) que indique claramente los horarios libres y ocupados de una cancha. | Cliente |
| **RF-06** | Reservas | El sistema debe permitir seleccionar un bloque de tiempo disponible y confirmar la reserva, guardando los datos en el sistema. | Cliente |
| **RF-07** | Perfil | El sistema debe permitir acceder a una sección donde se pueda visualizar el detalle y estado de las reservas actuales y pasadas. | Cliente |
| **RF-08** | Gestión | El sistema debe permitir al administrador visualizar un listado general de todas las reservas del complejo y cambiar su estado, como confirmada, cancelada o completada. | Administrador |
| **RF-09** | Gestión | El sistema debe permitir bloquear fechas u horarios específicos para que no puedan ser reservados en caso de mantenimiento o cierre de la cancha. | Administrador |

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

## 5. Escenarios de uso

| Usuario | Objetivo | Contexto | Secuencia | Resultado esperado |
| :--- | :--- | :--- | :--- | :--- |
| **Cliente / Administrador** | Registrarse en el sistema | Un usuario nuevo (o trabajador) quiere usar la plataforma por primera vez | Accede al formulario de registro → ingresa nombre, correo, teléfono, contraseña (y opcionalmente código de empleado) → confirma el registro | Se crea la cuenta con el rol correspondiente y el usuario puede iniciar sesión |
| Cliente | Reservar una cancha | El cliente quiere jugar fútbol el sábado por la tarde | Inicia sesión → busca canchas filtrando por deporte y fecha → visualiza calendario → selecciona horario disponible → confirma reserva | La reserva queda registrada y el horario pasa a "ocupado" |
| Cliente | Cancelar una reserva | El cliente no podrá asistir al horario reservado | Inicia sesión → accede a "Mis reservas" → selecciona la reserva → elige cancelar → confirma | La reserva cambia a "cancelada" y el horario vuelve a estar disponible |
| Cliente | Consultar historial de reservas | El cliente quiere revisar sus reservas pasadas y próximas | Inicia sesión → accede a la sección "Historial" → visualiza lista de reservas con su estado | El cliente puede consultar el detalle y estado de cada reserva |
| Cliente | Filtrar canchas por precio y horario | El cliente tiene un presupuesto limitado y un horario específico disponible | Ingresa al buscador → aplica filtros de deporte, fecha, horario y precio → revisa resultados | Se muestra una lista de canchas que cumplen con los criterios seleccionados |
| Administrador | Iniciar sesión en el panel administrativo | El administrador necesita gestionar las canchas y reservas | Ingresa sus credenciales → el sistema valida el rol de administrador | Accede al panel administrativo con las opciones de gestión |
| Administrador | Agregar una nueva cancha | El complejo deportivo incorpora una nueva instalación | Accede al panel → selecciona "Agregar cancha" → completa nombre, deporte, precio, ubicación y condiciones → guarda | La nueva cancha aparece en el catálogo disponible para los clientes |
| Administrador | Editar información de una cancha | El administrador necesita cambiar el precio o las condiciones de una cancha existente | Accede al catálogo → selecciona la cancha → edita los campos necesarios → guarda los cambios | La información actualizada se refleja en el sistema |
| Administrador | Desactivar una cancha | Una cancha deja de estar disponible para los clientes | Accede al catálogo → selecciona la cancha → cambia su estado a no disponible → guarda | La cancha deja de aparecer como disponible para nuevas reservas |
| Administrador | Bloquear horario por mantenimiento | Una cancha presenta daños y debe repararse durante dos días | Accede a la gestión de la cancha → selecciona bloquear fechas u horarios → indica el rango → guarda | Los horarios bloqueados dejan de estar disponibles para nuevas reservas |
| Administrador | Cambiar el estado de una reserva | El administrador debe marcar una reserva como completada después de finalizar el uso de la cancha | Accede al listado de reservas → selecciona la reserva → cambia su estado (confirmada, cancelada o completada) → guarda | El estado de la reserva queda actualizado en el sistema |

