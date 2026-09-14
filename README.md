# Sistema Web para Reserva de Canchas e Instalaciones Deportivas

## 1\. Descripción del proyecto

* **Nombre:** Sistema web para reserva de canchas e instalaciones deportivas
* **Problema:** La dificultad y pérdida de tiempo que enfrentan los usuarios al intentar encontrar canchas disponibles debido a la falta de información centralizada. Asimismo, la ineficiencia de los administradores de los complejos deportivos al llevar el control de reservas, horarios y cancelaciones de manera manual.
* **Propósito:** Proporcionar un sistema digitalizado y centralizar la información respecto a la reserva de canchas.
* **Objetivo general:** Diseñar e implementar una plataforma web centralizada que mejore la experiencia de los usuarios en la búsqueda y reserva de canchas deportivas, garantizando el acceso a información actualizada y detallada sobre las instalaciones en todo momento.
* **Alcance:** El proyecto abarcará el diseño y desarrollo de una aplicación web responsiva. Incluirá un catálogo digital de instalaciones deportivas con sus respectivos detalles (costos, ubicación y condiciones). Contará con un módulo para clientes (orientado a la consulta de disponibilidad y generación de reservas) y un módulo administrativo (para la gestión de canchas y control de las reservas agendadas).
* **Principales funcionalidades:**

  * Registro y autenticación de usuarios (perfil cliente y perfil administrador).
  * Buscador de canchas con filtros por tipo de deporte y disponibilidad de fechas/horarios.
  * Calendario interactivo para visualizar horarios libres y ocupados en tiempo real.
  * Sistema de generación, confirmación y cancelación de reservas.
  * Panel de administración para agregar/editar la información de las canchas y gestionar el estado de las reservas.

## 2\. Identificación de usuarios

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

  * Mantener un control organizado y centralizado de todas las reservas del día para evitar el "choque" o cruce de horarios (dos personas reservando la misma cancha).
  * Poder bloquear horarios si una cancha entra en reparación o mantenimiento.
  * Tener acceso a los datos de contacto del cliente en caso de que ocurra algún inconveniente con la reserva.
* **Funciones principales en el sistema:**

  * Iniciar sesión en un panel de control privado (Dashboard).
  * Gestionar el catálogo de instalaciones: Agregar nuevas canchas, editar su información (precios, fotos, estado) o eliminarlas.
  * Visualizar un listado completo o calendario con todas las reservas agendadas por los clientes.
  * Cambiar el estado de las reservas (ej. confirmada, cancelada, completada).
  * Bloquear manualmente horarios de las canchas por motivos de cierre o mantenimiento.

## 3\. Requisitos funcionales

|Código|Módulo|Descripción del Requisito|Usuario|
|-|-|-|-|
|**RF-01**|Seguridad|El sistema debe permitir a los usuarios nuevos registrarse creando una cuenta con sus datos personales (nombre, correo, teléfono y contraseña).|Cliente|
|**RF-02**|Seguridad|El sistema debe permitir el inicio de sesión seguro utilizando el correo electrónico y contraseña.|Ambos|
|**RF-03**|Catálogo|El sistema debe permitir agregar, editar, visualizar y eliminar (CRUD) la información de las canchas deportivas, incluyendo nombre, deporte, precio, ubicación, condiciones y estado.|Administrador|
|**RF-04**|Búsqueda|El sistema debe permitir buscar canchas filtrando los resultados por tipo de deporte, fecha, horario y precio.|Cliente|
|**RF-05**|Reservas|El sistema debe mostrar una interfaz (calendario o bloques de tiempo) que indique claramente los horarios libres y ocupados de una cancha.|Cliente|
|**RF-06**|Reservas|El sistema debe permitir seleccionar un bloque de tiempo disponible y confirmar la reserva, guardando los datos en el sistema.|Cliente|
|**RF-07**|Perfil|El sistema debe permitir acceder a una sección donde se pueda visualizar el detalle y estado de las reservas actuales y pasadas.|Cliente|
|**RF-08**|Gestión|El sistema debe permitir al administrador visualizar un listado general de todas las reservas del complejo y cambiar su estado, como confirmada, cancelada o completada.|Administrador|
|**RF-09**|Gestión|El sistema debe permitir bloquear fechas u horarios específicos para que no puedan ser reservados en caso de mantenimiento o cierre de la cancha.|Administrador|

## 4\. Requisitos no funcionales

