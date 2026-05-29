# Capítulo III: Requirements Specification

## 3.1 User Stories

En esta sección se presenta el conjunto de Epics y User Stories que especifican los requisitos funcionales de la plataforma FullTank. Las historias cubren tres categorías: User Stories para la Web Application (segmentos solicitante y proveedor), User Stories para el Landing Page (rol visitante) y Technical Stories para el RESTful API (rol Developer). Los criterios de aceptación siguen la estructura Gherkin (Given-When-Then), están redactados en presente y tercera persona, y no referencian detalles de interfaz.

<table border>
  <thead>
    <tr>
      <th>ID</th>
      <th>Título</th>
      <th>Descripción</th>
      <th>Criterios de Aceptación</th>
      <th>Epic ID</th>
    </tr>
  </thead>
  <tbody>
<!-- EP01 -->
<tr>
  <td colspan="5"><b>EP01 — Landing Page:</b> Funcionalidades visibles para visitantes en el sitio web público de FullTank: home, about us, how it works, beneficios, clientes, precios y contacto.</td>
</tr>
<tr>
  <td>US-01</td>
  <td>Ver sección Home</td>
  <td>Como visitante (proveedor), quiero ver una sección de inicio que resuma el valor de FullTank para comprender rápidamente el objetivo del sistema.</td>
  <td><b>Escenario 1: Visualización de resumen del sistema</b><br/>Dado que el visitante (proveedor) accede al sitio web,<br/>Cuando se encuentra en la sección Home,<br/>Entonces puede ver un resumen claro del sistema.<br/><br/><b>Escenario 2: Acceso a call to action desde Home</b><br/>Dado que el visitante (proveedor) revisa la sección Home,<br/>Cuando se solicita más información,<br/>Entonces el sistema presenta el resumen de ventajas de FullTank.</td>
  <td>EP01</td>
</tr>
<tr>
  <td>US-02</td>
  <td>Ver sección About Us</td>
  <td>Como visitante de ambos segmentos, quiero conocer quiénes están detrás de FullTank para confiar en el sistema.</td>
  <td><b>Escenario 1: Información visible del equipo</b><br/>Dado que el visitante de ambos segmentos accede a About Us,<br/>Cuando se carga la sección,<br/>Entonces puede leer una descripción del equipo detrás del sistema.<br/><br/><b>Escenario 2: Ver valores o misión</b><br/>Dado que el visitante de ambos segmentos revisa la sección completa,<br/>Cuando llega al final del contenido,<br/>Entonces puede conocer los valores o misión de la empresa.</td>
  <td>EP01</td>
</tr>
<tr>
  <td>US-03</td>
  <td>Ver sección How it works?</td>
  <td>Como visitante de ambos segmentos, quiero entender cómo funciona FullTank paso a paso para evaluar si se ajusta a mis necesidades.</td>
  <td><b>Escenario 1: Comprensión del flujo de pedidos</b><br/>Dado que el visitante de ambos segmentos accede a How it works?,<br/>Cuando lee la sección,<br/>Entonces entiende el flujo de pedido desde solicitud hasta entrega.<br/><br/><b>Escenario 2: Interacción clara entre usuarios</b><br/>Dado que el visitante de ambos segmentos busca claridad,<br/>Cuando revisa la sección,<br/>Entonces puede comprender cómo interactúan solicitante y proveedor.</td>
  <td>EP01</td>
</tr>
<tr>
  <td>US-04</td>
  <td>Enviar mensaje de contacto</td>
  <td>Como visitante de ambos segmentos, quiero enviar un mensaje desde Contact Us para solicitar más información.</td>
  <td><b>Escenario 1: Envío exitoso de mensaje</b><br/>Dado que el visitante de ambos segmentos completa el formulario correctamente,<br/>Cuando el formulario es enviado con datos válidos,<br/>Entonces el mensaje es registrado para revisión.<br/><br/><b>Escenario 2: Validación de campos obligatorios</b><br/>Dado que el visitante de ambos segmentos deja campos vacíos,<br/>Cuando intenta el envío del formulario,<br/>Entonces el sistema muestra una advertencia.<br/><br/><b>Escenario 3: Confirmación de envío</b><br/>Dado que el visitante de ambos segmentos envía el formulario exitosamente,<br/>Cuando el mensaje es registrado,<br/>Entonces el sistema confirma el registro del mensaje.</td>
  <td>EP01</td>
</tr>
<tr>
  <td>US-36</td>
  <td>Ver sección Benefits</td>
  <td>Como visitante de ambos segmentos, quiero conocer las principales ventajas con las que puedo contar para evaluar la implementación de la plataforma.</td>
  <td><b>Escenario 1: Visualizar beneficios</b><br/>Dado que el visitante de ambos segmentos accede a la sección de beneficios de FullTank,<br/>Cuando visualiza los múltiples beneficios,<br/>Entonces puede identificar las ventajas de la plataforma frente a sus competidores.<br/><br/><b>Escenario 2: Identificar valor de la plataforma</b><br/>Dado que el visitante de ambos segmentos accede a la sección de beneficios de FullTank,<br/>Cuando observa la lista de beneficios,<br/>Entonces ve cómo le podría beneficiar usar FullTank.</td>
  <td>EP01</td>
</tr>
<tr>
  <td>US-37</td>
  <td>Ver sección Testimonios de Clientes</td>
  <td>Como visitante de ambos segmentos, quiero conocer los testimonios de los usuarios de FullTank para tener confianza en la plataforma y saber que otras empresas ya la están usando.</td>
  <td><b>Escenario 1: Ver testimonios de clientes</b><br/>Dado que el visitante de ambos segmentos está interesado en los comentarios de los clientes,<br/>Cuando accede a la sección de testimonios de FullTank,<br/>Entonces puede leer un breve testimonio sobre experiencias usando FullTank.<br/><br/><b>Escenario 2: Visualizar testimonios recientes</b><br/>Dado que el visitante de ambos segmentos accede a la sección de testimonios y esta se actualiza regularmente,<br/>Cuando se carga la información,<br/>Entonces visualiza los últimos testimonios de clientes que se han unido a FullTank.<br/><br/><b>Escenario 3: Error de carga</b><br/>Dado que ocurre un error al cargar los testimonios,<br/>Cuando se solicita la visualización de la sección,<br/>Entonces se muestra un mensaje genérico de error sin interrumpir la navegación.</td>
  <td>EP01</td>
</tr>
<tr>
  <td>US-38</td>
  <td>Ver sección Planes y Precios</td>
  <td>Como visitante (ambos segmentos), quiero saber qué planes se adecuan a mis necesidades para poder iniciar un proceso de registro o solicitud.</td>
  <td><b>Escenario 1: Ver información sobre ser solicitante de combustible</b><br/>Dado que el visitante solicita ver los planes y precios,<br/>Cuando visualiza los diferentes precios y las características incluidas,<br/>Entonces entiende que existe flexibilidad para adaptar FullTank a su empresa.<br/><br/><b>Escenario 2: Selección de plan y redirección</b><br/>Dado que el visitante está interesado en obtener un plan específico,<br/>Cuando el usuario selecciona un plan,<br/>Entonces es redirigido a la página de registro.<br/><br/><b>Escenario 3: Visualización en móvil</b><br/>Dado que el visitante accede desde un dispositivo móvil,<br/>Cuando se solicita la carga de la sección,<br/>Entonces los planes se muestran de forma legible y adaptada a la pantalla.</td>
  <td>EP01</td>
</tr>
<tr>
  <td>US-39</td>
  <td>Cambiar idioma de la plataforma</td>
  <td>Como visitante de ambos segmentos, quiero poder cambiar entre inglés y español para entender la plataforma en mi idioma preferido.</td>
  <td><b>Escenario 1: Cambiar idioma a español</b><br/>Dado que el visitante de ambos segmentos está viendo la página en inglés,<br/>Cuando selecciona la opción de español,<br/>Entonces toda la interfaz de la página se muestra en español.<br/><br/><b>Escenario 2: Cambiar idioma a inglés</b><br/>Dado que el visitante está viendo la página en español,<br/>Cuando selecciona la opción de inglés,<br/>Entonces toda la interfaz de la página se muestra en inglés.<br/><br/><b>Escenario 3: Persistencia del idioma</b><br/>Dado que el visitante cambia el idioma y navega a otra sección,<br/>Cuando regresa a la sección anterior,<br/>Entonces el idioma seleccionado se mantiene activo.</td>
  <td>EP01</td>


<!-- EP02 -->
<tr>
  <td colspan="5"><b>EP02 — Gestión de Pedidos (Solicitante):</b> Permite al solicitante registrar, consultar, confirmar y gestionar sus pedidos de combustible, incluyendo pagos e historial.</td>
</tr>
<tr>
  <td>US-05</td>
  <td>Registrar nuevo pedido</td>
  <td>Como solicitante, quiero registrar un pedido con tipo y cantidad de combustible para que el proveedor lo procese.</td>
  <td><b>Escenario 1: Registro exitoso del pedido</b><br/>Dado que el solicitante accede al formulario de pedidos,<br/>Cuando completa los campos requeridos,<br/>Entonces puede enviar un nuevo pedido.<br/><br/><b>Escenario 2: Validación de campos</b><br/>Dado que el solicitante deja un campo obligatorio vacío,<br/>Cuando intenta enviar el pedido,<br/>Entonces el sistema muestra un mensaje de error.<br/><br/><b>Escenario 3: Confirmación del cambio de estado</b><br/>Dado que el solicitante envió el pedido,<br/>Cuando el proveedor lo aprueba,<br/>Entonces su estado se actualiza automáticamente.</td>
  <td>EP02</td>
</tr>
<tr>
  <td>US-06</td>
  <td>Consultar estado del pedido</td>
  <td>Como solicitante, quiero ver el estado de mis pedidos para saber si están aprobados, en tránsito o entregados.</td>
  <td><b>Escenario 1: Consulta de estado en el panel</b><br/>Dado que el solicitante accede a su panel,<br/>Cuando revisa la lista de pedidos,<br/>Entonces ve el estado actualizado.<br/><br/><b>Escenario 2: Actualización dinámica de estado</b><br/>Dado que el solicitante está visualizando el panel de pedidos,<br/>Cuando el pedido cambia de estado,<br/>Entonces el cambio se refleja correctamente al recargar el panel.</td>
  <td>EP02</td>
</tr>
<tr>
  <td>US-07</td>
  <td>Confirmar recepción de pedido</td>
  <td>Como solicitante, quiero confirmar que recibí el pedido para que el proveedor lo cierre.</td>
  <td><b>Escenario 1: Confirmación exitosa de recepción</b><br/>Dado que el solicitante recibió el pedido,<br/>Cuando lo confirma en el sistema,<br/>Entonces su estado cambia a "Entregado".<br/><br/><b>Escenario 2: Prevención de doble confirmación</b><br/>Dado que el solicitante ya confirmó la entrega,<br/>Cuando intenta volver a confirmar,<br/>Entonces el sistema bloquea la acción y notifica al usuario.</td>
  <td>EP02</td>
</tr>
<tr>
  <td>US-08</td>
  <td>Registrar información de pago</td>
  <td>Como solicitante, quiero ingresar la información de los pagos correspondientes para validar el pedido ante el proveedor.</td>
  <td><b>Escenario 1: Registro exitoso de depósitos</b><br/>Dado que el solicitante ingresa la información de depósitos,<br/>Cuando registra el pedido,<br/>Estos quedan vinculados a él.<br/><br/><b>Escenario 2: Validación del formulario de ingreso de depósitos</b><br/>Dado que el solicitante intenta ingresar los datos del depósito,<br/>Cuando excede el límite de caracteres,<br/>Entonces el sistema muestra un mensaje de error.<br/><br/><b>Escenario 3: Validación de depósitos ya registrados</b><br/>Dado que el solicitante ingresa un depósito con un número de operación repetido,<br/>Cuando intenta seguir con el registro,<br/>Entonces el sistema notifica el error.</td>
  <td>EP02</td>
</tr>
<tr>
  <td>US-09</td>
  <td>Ver historial de pedidos</td>
  <td>Como solicitante, quiero ver mis pedidos anteriores para tener control sobre mi consumo.</td>
  <td><b>Escenario 1: Visualización del historial</b><br/>Dado que el solicitante accede al historial,<br/>Cuando se listan los pedidos,<br/>Entonces puede ver fecha, tipo y estado de cada uno.<br/><br/><b>Escenario 2: Historial vacío</b><br/>Dado que el solicitante aún no ha realizado pedidos,<br/>Cuando accede al historial,<br/>Entonces se muestra un mensaje informativo.<br/><br/><b>Escenario 3: Acceso a detalles desde historial</b><br/>Dado que el solicitante ve la lista de pedidos anteriores,<br/>Cuando selecciona uno,<br/>Entonces puede revisar sus detalles.</td>
  <td>EP02</td>
</tr>
<tr>
  <td>US-43</td>
  <td>Ver detalle de pedido</td>
  <td>Como usuario de ambos segmentos, quiero ver el detalle completo de un pedido para revisar toda la información asociada.</td>
  <td><b>Escenario 1: Visualización completa del detalle</b><br/>Dado que el usuario selecciona un pedido desde su panel,<br/>Cuando se carga la vista de detalle,<br/>Entonces puede ver tipo de combustible, cantidad, estado, fechas, datos de pago y asignación logística.<br/><br/><b>Escenario 2: Pedido no encontrado</b><br/>Dado que el usuario intenta acceder al detalle de un pedido inexistente,<br/>Cuando se carga la vista,<br/>Entonces el sistema muestra un mensaje de error y ofrece regresar al listado.<br/><br/><b>Escenario 3: Restricción de acceso a pedidos ajenos</b><br/>Dado que el usuario intenta acceder al detalle de un pedido que no le pertenece,<br/>Cuando carga la URL directamente,<br/>Entonces el sistema restringe el acceso y redirige a su propio panel.</td>
  <td>EP02</td>
</tr>

<!-- EP03 -->
<tr>
  <td colspan="5"><b>EP03 — Gestión de Pedidos (Proveedor):</b> Permite al proveedor ver, aprobar, rechazar, despachar, cerrar pedidos y generar reportes de ventas.</td>
</tr>
<tr>
  <td>US-10</td>
  <td>Ver pedidos pendientes</td>
  <td>Como proveedor, quiero ver todos los pedidos pendientes para analizarlos y tomar acción.</td>
  <td><b>Escenario 1: Listado de pedidos pendientes</b><br/>Dado que el proveedor accede al panel,<br/>Cuando ve los pedidos pendientes,<br/>Entonces puede revisar sus detalles básicos.<br/><br/><b>Escenario 2: Filtro por fechas o cliente</b><br/>Dado que el proveedor tiene muchos pedidos,<br/>Cuando aplica filtros por fecha o empresa,<br/>Entonces puede localizar los pedidos relevantes.</td>
  <td>EP03</td>
</tr>
<tr>
  <td>US-11</td>
  <td>Aprobar pedido</td>
  <td>Como proveedor, quiero aprobar pedidos según los depósitos hechos a mis cuentas bancarias.</td>
  <td><b>Escenario 1: Aprobación de pedido con depósitos válidos</b><br/>Dado que el proveedor tiene el pago completo del pedido,<br/>Cuando intenta aprobarlo,<br/>Entonces el estado cambia a "Aprobado".<br/><br/><b>Escenario 2: No aprobar el pedido por pago incompleto</b><br/>Dado que el proveedor no cuenta con los depósitos suficientes para completar el pago del pedido,<br/>Cuando intenta aprobarlo,<br/>Entonces se muestra un mensaje indicando que el pedido no fue pagado por completo.</td>
  <td>EP03</td>
</tr>
<tr>
  <td>US-12</td>
  <td>Marcar pedido como despachado</td>
  <td>Como proveedor, quiero marcar cuándo un pedido sale a entrega para notificar al cliente.</td>
  <td><b>Escenario 1: Despacho exitoso de un pedido</b><br/>Dado que el proveedor tiene un pedido aprobado,<br/>Cuando marca el pedido como despachado,<br/>Entonces el estado cambia a "Despachado".<br/><br/><b>Escenario 2: Restricción de despacho sin aprobación previa</b><br/>Dado que el proveedor intenta despachar un pedido sin pasar por la liberación correspondiente,<br/>Cuando ejecuta la acción,<br/>Entonces el sistema impide el cambio de estado y muestra un mensaje.</td>
  <td>EP03</td>
</tr>
<tr>
  <td>US-13</td>
  <td>Cerrar pedido</td>
  <td>Como proveedor, quiero cerrar el pedido cuando el cliente confirme la entrega para finalizar el proceso.</td>
  <td><b>Escenario 1: Cierre correcto del pedido tras confirmación</b><br/>Dado que el solicitante ya confirmó la entrega,<br/>Cuando el proveedor cierra el pedido,<br/>Entonces este no puede modificarse más.<br/><br/><b>Escenario 2: Intento de cierre sin confirmación previa</b><br/>Dado que el proveedor intenta cerrar el pedido,<br/>Cuando el solicitante aún no ha confirmado la entrega,<br/>Entonces el sistema impide esta acción.</td>
  <td>EP03</td>
</tr>
<tr>
  <td>US-14</td>
  <td>Generar reporte de ventas</td>
  <td>Como proveedor, quiero generar reportes de ventas para tener registro de operaciones realizadas.</td>
  <td><b>Escenario 1: Generación de reporte con datos disponibles</b><br/>Dado que el proveedor selecciona un rango de fechas válido,<br/>Cuando solicita el reporte,<br/>Entonces se genera un archivo con los datos de ventas.<br/><br/><b>Escenario 2: Generación sin datos en el rango</b><br/>Dado que el proveedor selecciona un rango sin ventas,<br/>Cuando solicita el reporte,<br/>Entonces el sistema informa que no hay resultados.<br/><br/><b>Escenario 3: Descarga del archivo generado</b><br/>Dado que el reporte se genera correctamente,<br/>Cuando finaliza el proceso,<br/>Entonces el proveedor puede descargar el archivo.</td>
  <td>EP03</td>
</tr>
<tr>
  <td>US-42</td>
  <td>Rechazar pedido</td>
  <td>Como proveedor, quiero rechazar un pedido cuando no pueda atenderlo para notificar al solicitante oportunamente.</td>
  <td><b>Escenario 1: Rechazo exitoso con motivo</b><br/>Dado que el proveedor decide no atender un pedido pendiente,<br/>Cuando registra el rechazo e ingresa un motivo,<br/>Entonces el estado del pedido cambia a "Rechazado" y el solicitante recibe una notificación.<br/><br/><b>Escenario 2: Intento de rechazo sin motivo</b><br/>Dado que el proveedor intenta rechazar un pedido sin ingresar motivo,<br/>Cuando ejecuta la acción,<br/>Entonces el sistema solicita ingresar un motivo obligatorio antes de confirmar.<br/><br/><b>Escenario 3: Rechazo de pedido ya procesado</b><br/>Dado que el proveedor intenta rechazar un pedido que ya fue aprobado o despachado,<br/>Cuando ejecuta la acción,<br/>Entonces el sistema impide la acción y muestra el estado actual del pedido.</td>
  <td>EP03</td>
</tr>

<!-- EP04 -->
<tr>
  <td colspan="5"><b>EP04 — Autenticación y Registro:</b> Registro de empresas solicitantes y proveedoras, inicio de sesión, recuperación y cierre de sesión.</td>
</tr>
<tr>
  <td>US-15</td>
  <td>Iniciar sesión</td>
  <td>Como usuario registrado, quiero iniciar sesión con correo y contraseña para acceder a mi cuenta.</td>
  <td><b>Escenario 1: Inicio de sesión exitoso</b><br/>Dado que el usuario registrado ingresa credenciales válidas,<br/>Cuando envía las credenciales de acceso,<br/>Entonces accede a su dashboard.<br/><br/><b>Escenario 2: Error por credenciales incorrectas</b><br/>Dado que el usuario registrado ingresa datos incorrectos,<br/>Cuando intenta iniciar sesión,<br/>Entonces el sistema muestra un mensaje de error.<br/><br/><b>Escenario 3: Validación de campos vacíos</b><br/>Dado que el usuario deja campos vacíos,<br/>Cuando intenta iniciar sesión,<br/>Entonces el sistema solicita completar los campos.</td>
  <td>EP04</td>
</tr>
<tr>
  <td>US-16</td>
  <td>Recuperar contraseña</td>
  <td>Como usuario registrado, quiero recuperar mi contraseña para volver a acceder si la olvidé.</td>
  <td><b>Escenario 1: Envío de enlace de recuperación</b><br/>Dado que el usuario registrado ingresa su correo válido,<br/>Cuando solicita recuperación,<br/>Entonces recibe un enlace al correo.<br/><br/><b>Escenario 2: Error por correo no registrado</b><br/>Dado que el usuario ingresa un correo inexistente,<br/>Cuando solicita recuperación,<br/>Entonces se le informa que el correo no está registrado.<br/><br/><b>Escenario 3: Validación de campo vacío</b><br/>Dado que el usuario no completa el campo de correo,<br/>Cuando intenta enviar la solicitud,<br/>Entonces el sistema solicita completarlo.</td>
  <td>EP04</td>
</tr>
<tr>
  <td>US-17</td>
  <td>Cerrar sesión</td>
  <td>Como usuario registrado, quiero poder cerrar sesión para mantener segura mi cuenta.</td>
  <td><b>Escenario 1: Cierre exitoso de sesión</b><br/>Dado que el usuario está autenticado,<br/>Cuando solicita el cierre de sesión,<br/>Entonces la sesión se finaliza y es redirigido al login.<br/><br/><b>Escenario 2: Confirmación de cierre de sesión</b><br/>Dado que el usuario cierra sesión,<br/>Cuando termina la acción,<br/>Entonces el sistema muestra un mensaje de despedida o confirmación.</td>
  <td>EP04</td>
</tr>
<tr>
  <td>US-40</td>
  <td>Registrar empresa solicitante</td>
  <td>Como visitante (solicitante), quiero registrar mi empresa en la plataforma para comenzar a realizar pedidos de combustible.</td>
  <td><b>Escenario 1: Registro exitoso de empresa</b><br/>Dado que el visitante completa todos los campos requeridos del formulario de registro,<br/>Cuando envía el formulario de registro,<br/>Entonces se crea la cuenta y es redirigido a su dashboard.<br/><br/><b>Escenario 2: RUC o correo ya registrado</b><br/>Dado que el visitante ingresa un RUC o correo que ya existe en el sistema,<br/>Cuando intenta completar el registro,<br/>Entonces el sistema muestra un mensaje indicando que ya existe una cuenta con esos datos.<br/><br/><b>Escenario 3: Campos obligatorios vacíos</b><br/>Dado que el visitante deja uno o más campos obligatorios sin completar,<br/>Cuando intenta continuar con el registro,<br/>Entonces el sistema resalta los campos faltantes y solicita completarlos.</td>
  <td>EP04</td>
</tr>
<tr>
  <td>US-41</td>
  <td>Registrar empresa proveedora</td>
  <td>Como visitante (proveedor), quiero registrar mi empresa distribuidora en la plataforma para comenzar a gestionar pedidos de combustible.</td>
  <td><b>Escenario 1: Registro exitoso de proveedor</b><br/>Dado que el visitante proveedor completa todos los campos del formulario,<br/>Cuando confirma el registro,<br/>Entonces se crea la cuenta y puede acceder a su panel de gestión.<br/><br/><b>Escenario 2: Datos de empresa duplicados</b><br/>Dado que el visitante ingresa un RUC que ya está registrado como proveedor,<br/>Cuando intenta finalizar el registro,<br/>Entonces el sistema notifica que ya existe una empresa con ese RUC.<br/><br/><b>Escenario 3: Formato inválido en campos</b><br/>Dado que el visitante ingresa datos con formato incorrecto,<br/>Cuando intenta avanzar en el formulario,<br/>Entonces el sistema muestra un mensaje de validación por campo.</td>
  <td>EP04</td>
</tr>

<!-- EP05 -->
<tr>
  <td colspan="5"><b>EP05 — Dashboard y Resumen Operativo:</b> Paneles de control con KPIs y resúmenes de estado de pedidos para ambos segmentos.</td>
</tr>
<tr>
  <td>US-18</td>
  <td>Ver resumen de pedidos (Solicitante)</td>
  <td>Como solicitante, quiero ver un resumen de mis pedidos para identificar cuántos están en proceso o completados.</td>
  <td><b>Escenario 1: Visualización de resumen con datos disponibles</b><br/>Dado que el solicitante tiene pedidos registrados,<br/>Cuando accede a su dashboard,<br/>Entonces visualiza los KPIs por estado: pendientes, aprobados, despachados, finalizados y rechazados.<br/><br/><b>Escenario 2: Sin pedidos registrados</b><br/>Dado que el solicitante no tiene pedidos,<br/>Cuando accede al dashboard,<br/>Entonces ve un mensaje informando "No hay pedidos registrados".<br/><br/><b>Escenario 3: Error al cargar datos del resumen</b><br/>Dado que el solicitante accede al dashboard,<br/>Cuando ocurre un error de carga,<br/>Entonces el sistema muestra un mensaje e intenta recargar los datos automáticamente.</td>
  <td>EP05</td>
</tr>
<tr>
  <td>US-19</td>
  <td>Ver resumen de pedidos (Proveedor)</td>
  <td>Como proveedor, quiero ver un resumen de pedidos gestionados y pendientes para organizar a los clientes.</td>
  <td><b>Escenario 1: Visualización de KPIs con datos</b><br/>Dado que el proveedor tiene pedidos registrados,<br/>Cuando accede a su dashboard,<br/>Entonces ve KPIs de pedidos: pendientes, aprobados, rechazados, despachados y finalizados.<br/><br/><b>Escenario 2: Sin datos registrados</b><br/>Dado que no hay pedidos registrados,<br/>Cuando se carga el dashboard,<br/>Entonces los KPIs se muestran con valor cero y un mensaje informativo.<br/><br/><b>Escenario 3: Fallo en la carga del resumen</b><br/>Dado que el proveedor accede al dashboard,<br/>Cuando hay un error de conexión,<br/>Entonces se muestra una alerta con opción para reintentar.</td>
  <td>EP05</td>
</tr>

<!-- EP06 -->
<tr>
  <td colspan="5"><b>EP06 — Logística y Despacho:</b> Gestión de flota: vehículos, conductores, asignación y validación de disponibilidad para despachos.</td>
</tr>
<tr>
  <td>US-20</td>
  <td>Asignar vehículo a pedido</td>
  <td>Como proveedor, quiero asignar un vehículo a un pedido aprobado para organizar la logística.</td>
  <td><b>Escenario 1: Asignación válida</b><br/>Dado que el proveedor tiene un pedido aprobado y un vehículo libre disponible,<br/>Cuando selecciona el vehículo para asignarlo,<br/>Entonces queda asignado correctamente al pedido.<br/><br/><b>Escenario 2: Vehículo ocupado</b><br/>Dado que el proveedor intenta asignar un vehículo que ya está ocupado,<br/>Cuando realiza la acción,<br/>Entonces el sistema muestra un mensaje indicando que el vehículo no está disponible.<br/><br/><b>Escenario 3: Falla durante la asignación</b><br/>Dado que el proveedor intenta asignar un vehículo y ocurre un error en el backend,<br/>Cuando se ejecuta la asignación,<br/>Entonces se muestra un mensaje de error y no se vincula ningún vehículo.</td>
  <td>EP06</td>
</tr>
<tr>
  <td>US-21</td>
  <td>Asignar conductor a pedido</td>
  <td>Como proveedor, quiero asignar un conductor para completar la información de despacho.</td>
  <td><b>Escenario 1: Conductor disponible</b><br/>Dado que el proveedor tiene un pedido con vehículo asignado y el conductor está libre,<br/>Cuando selecciona al conductor,<br/>Entonces este se vinculan correctamente al pedido.<br/><br/><b>Escenario 2: Conductor ya asignado en misma franja horaria</b><br/>Dado que el conductor está asignado a otro pedido en el mismo horario,<br/>Cuando se intenta asignarlo,<br/>Entonces el sistema bloquea la acción y muestra un mensaje de conflicto.<br/><br/><b>Escenario 3: Error al guardar</b><br/>Dado que el proveedor intenta guardar la asignación y ocurre una falla técnica,<br/>Cuando realiza la acción,<br/>Entonces se muestra un mensaje de error y no se realiza el vínculo.</td>
  <td>EP06</td>
</tr>
<tr>
  <td>US-22</td>
  <td>Validar disponibilidad de transporte</td>
  <td>Como proveedor, quiero saber qué vehículos están disponibles antes de asignarlos para vincularlos correctamente.</td>
  <td><b>Escenario 1: Vehículo no disponible por superposición</b><br/>Dado que el proveedor visualiza el listado de vehículos,<br/>Cuando un vehículo está asignado a otro pedido para la misma fecha y hora estimada,<br/>Entonces el sistema lo muestra como no disponible.<br/><br/><b>Escenario 2: Vehículo disponible</b><br/>Dado que el proveedor visualiza un vehículo sin conflictos de agenda,<br/>Cuando se carga el listado de vehículos,<br/>Entonces dicho vehículo se muestra como seleccionable.<br/><br/><b>Escenario 3: Conflicto en tiempo real</b><br/>Dado que el proveedor intenta seleccionar un vehículo que fue asignado recientemente por otro usuario,<br/>Cuando realiza la acción,<br/>Entonces el sistema bloquea la selección y muestra un mensaje de actualización.</td>
  <td>EP06</td>
</tr>
<tr>
  <td>US-44</td>
  <td>Gestionar vehículos de flota</td>
  <td>Como proveedor, quiero registrar y administrar los vehículos de mi flota para tenerlos disponibles al momento de asignarlos a pedidos.</td>
  <td><b>Escenario 1: Registro exitoso de vehículo</b><br/>Dado que el proveedor accede al módulo de flota y completa los datos del vehículo,<br/>Cuando guarda el registro,<br/>Entonces el vehículo queda disponible para ser asignado a pedidos.<br/><br/><b>Escenario 2: Placa duplicada</b><br/>Dado que el proveedor intenta registrar un vehículo con una placa ya existente,<br/>Cuando intenta guardar,<br/>Entonces el sistema muestra un error indicando que la placa ya está registrada.<br/><br/><b>Escenario 3: Eliminación de vehículo</b><br/>Dado que el proveedor elimina un vehículo de la flota,<br/>Cuando confirma la acción,<br/>Entonces el vehículo deja de aparecer como opción en la asignación de pedidos.</td>
  <td>EP06</td>
</tr>
<tr>
  <td>US-45</td>
  <td>Gestionar conductores</td>
  <td>Como proveedor, quiero registrar y administrar los conductores de mi empresa para asignarlos correctamente a los despachos.</td>
  <td><b>Escenario 1: Registro exitoso de conductor</b><br/>Dado que el proveedor completa los datos del conductor (nombre, DNI, licencia),<br/>Cuando guarda el registro,<br/>Entonces el conductor queda disponible para ser asignado a pedidos.<br/><br/><b>Escenario 2: DNI duplicado</b><br/>Dado que el proveedor intenta registrar un conductor con un DNI ya existente,<br/>Cuando intenta guardar,<br/>Entonces el sistema notifica que el conductor ya está registrado.<br/><br/><b>Escenario 3: Edición de datos de conductor</b><br/>Dado que el proveedor actualiza los datos de un conductor existente,<br/>Cuando guarda los cambios,<br/>Entonces la información se actualiza correctamente en el sistema.</td>
  <td>EP06</td>
</tr>

<!-- EP07 -->
<tr>
  <td colspan="5"><b>EP07 — Perfil de Usuario:</b> Visualización y edición de datos del perfil del usuario autenticado.</td>
</tr>
<tr>
  <td>US-23</td>
  <td>Ver perfil de usuario</td>
  <td>Como usuario registrado, quiero ver mis datos de perfil para revisar mi información registrada.</td>
  <td><b>Escenario 1: Visualización exitosa del perfil</b><br/>Dado que el usuario tiene sesión activa,<br/>Cuando accede a su perfil,<br/>Entonces ve su nombre, correo y rol.<br/><br/><b>Escenario 2: Error en la carga de datos</b><br/>Dado que el usuario accede a su perfil y ocurre un error al obtener los datos,<br/>Cuando se carga la vista,<br/>Entonces se muestra un mensaje de error y se sugiere reintentar.<br/><br/><b>Escenario 3: Restricción de datos de otros usuarios</b><br/>Dado que el usuario tiene sesión activa,<br/>Cuando intenta ver otro perfil,<br/>Entonces el sistema restringe el acceso y muestra su propia información.</td>
  <td>EP07</td>
</tr>
<tr>
  <td>US-24</td>
  <td>Editar datos de perfil</td>
  <td>Como usuario registrado, quiero editar mis datos para mantener mi información actualizada.</td>
  <td><b>Escenario 1: Edición y guardado exitoso</b><br/>Dado que el usuario modifica uno o más campos del formulario,<br/>Cuando la información ingresada es válida,<br/>Entonces el sistema guarda los cambios correctamente.<br/><br/><b>Escenario 2: Campo obligatorio vacío</b><br/>Dado que el usuario deja un campo obligatorio vacío,<br/>Cuando intenta guardar,<br/>Entonces el sistema muestra un mensaje de validación indicando el campo requerido.<br/><br/><b>Escenario 3: Error del servidor al guardar</b><br/>Dado que el usuario intenta guardar y ocurre un fallo en el servidor,<br/>Cuando se realiza la acción,<br/>Entonces se muestra un mensaje de error y los datos ingresados permanecen visibles.</td>
  <td>EP07</td>
</tr>

<!-- EP08 -->
<tr>
  <td colspan="5"><b>EP08 — Soporte y Contacto:</b> Secciones de preguntas frecuentes e información de contacto rápido para usuarios y visitantes.</td>
</tr>
<tr>
  <td>US-25</td>
  <td>Ver sección de preguntas frecuentes</td>
  <td>Como visitante de ambos segmentos, quiero acceder a una sección de preguntas frecuentes para resolver dudas rápidamente.</td>
  <td><b>Escenario 1: Visualización de preguntas comunes</b><br/>Dado que el visitante solicita ver la sección de preguntas frecuentes,<br/>Cuando se carga el contenido,<br/>Entonces puede leer las preguntas y respuestas más frecuentes.<br/><br/><b>Escenario 2: Organización por categorías</b><br/>Dado que el visitante solicita ver la sección de preguntas frecuentes con muchas entradas,<br/>Cuando se organiza el contenido,<br/>Entonces puede visualizarlas clasificadas en categorías.<br/><br/><b>Escenario 3: Error al cargar FAQs</b><br/>Dado que el visitante solicita ver la sección y ocurre un fallo en la carga,<br/>Cuando intenta visualizar las preguntas frecuentes,<br/>Entonces se muestra un mensaje de error o un contenido informativo alternativo.<br/><br/><b>Escenario 4: Búsqueda de pregunta específica</b><br/>Dado que el visitante tiene una duda puntual,<br/>Cuando ingresa palabras clave de búsqueda de FAQs,<br/>Entonces se filtran las preguntas de manera dinámica.</td>
  <td>EP08</td>
</tr>
<tr>
  <td>US-26</td>
  <td>Acceder a información de contacto rápido</td>
  <td>Como usuario de ambos segmentos, quiero ver datos de contacto directo (teléfono o correo) para hacer consultas urgentes.</td>
  <td><b>Escenario 1: Visualización de datos de contacto</b><br/>Dado que el usuario solicita la visualización del soporte,<br/>Cuando se presenta la información,<br/>Entonces puede visualizar claramente el correo de soporte y número telefónico.<br/><br/><b>Escenario 2: Acceso al correo de cliente</b><br/>Dado que el usuario accede a la dirección de correo,<br/>Cuando tiene una aplicación de correo configurada,<br/>Entonces el sistema inicia la aplicación de correo predeterminada.<br/><br/><b>Escenario 3: Falla en la configuración de contacto</b><br/>Dado que el usuario accede a la página y los datos de contacto no están bien configurados,<br/>Cuando se carga la sección de contacto,<br/>Entonces el sistema muestra un mensaje genérico invitando a intentar más tarde.</td>
  <td>EP08</td>
</tr>

<!-- EP11 -->
<tr>
  <td colspan="5"><b>EP09 — Búsqueda y Filtrado:</b> Funcionalidades para buscar pedidos por código y filtrarlos por estado.</td>
</tr>
<tr>
  <td>US-27</td>
  <td>Buscar pedido por código</td>
  <td>Como usuario de ambos segmentos, quiero buscar un pedido específico por su código para encontrarlo rápidamente.</td>
  <td><b>Escenario 1: Pedido encontrado</b><br/>Dado que el usuario escribe un código válido,<br/>Cuando existe un pedido con ese código,<br/>Entonces se muestra el resultado correspondiente.<br/><br/><b>Escenario 2: Pedido no encontrado</b><br/>Dado que el usuario digita un código no correspondiente a ningún pedido,<br/>Cuando finaliza la búsqueda,<br/>Entonces el sistema muestra un mensaje de que no hay coincidencias.</td>
  <td>EP09</td>
</tr>
<tr>
  <td>US-28</td>
  <td>Filtrar pedidos por estado</td>
  <td>Como usuario de ambos segmentos, quiero filtrar mis pedidos por estado (pendiente, aprobado, entregado) para facilitar la revisión.</td>
  <td><b>Escenario 1: Aplicar filtro correctamente</b><br/>Dado que el usuario selecciona un estado,<br/>Cuando se aplica el filtro,<br/>Entonces solo se muestran los pedidos con ese estado.<br/><br/><b>Escenario 2: No hay pedidos en ese estado</b><br/>Dado que el usuario selecciona un estado que no tiene coincidencias,<br/>Cuando ejecuta el filtro,<br/>Entonces se muestra un mensaje indicando que no hay pedidos para ese estado.</td>
  <td>EP09</td>
</tr>

<!-- EP10 -->
<tr>
  <td colspan="5"><b>EP10 — Notificaciones:</b> Notificaciones automáticas al solicitante sobre cambios de estado de sus pedidos.</td>
</tr>
<tr>
  <td>US-29</td>
  <td>Recibir notificación de aprobación</td>
  <td>Como solicitante, quiero recibir una notificación cuando un pedido sea aprobado o rechazado para estar informado.</td>
  <td><b>Escenario 1: Visualización de notificación</b><br/>Dado que el proveedor cambia el estado del pedido,<br/>Cuando el solicitante inicia sesión,<br/>Entonces ve una notificación del evento.<br/><br/><b>Escenario 2: Pedido actualizado desde otra sesión</b><br/>Dado que el solicitante aún no ha leído la notificación,<br/>Cuando actualiza la interfaz,<br/>Entonces la notificación se mantiene visible hasta que sea marcada como leída.</td>
  <td>EP10</td>
</tr>
<tr>
  <td>US-30</td>
  <td>Notificación de pedido despachado</td>
  <td>Como solicitante, quiero recibir una notificación cuando un pedido haya sido despachado para estar informado.</td>
  <td><b>Escenario 1: Pedido marcado como despachado</b><br/>Dado que el proveedor marca el pedido como despachado,<br/>Cuando el solicitante consulta su cuenta,<br/>Entonces puede ver la notificación correspondiente.<br/><br/><b>Escenario 2: Visualización posterior del evento</b><br/>Dado que el pedido fue despachado anteriormente,<br/>Cuando el solicitante accede en otro momento,<br/>Entonces la notificación sigue disponible hasta ser archivada o leída.</td>
  <td>EP10</td>
</tr>

<!-- EP11 -->
<tr>
  <td colspan="5"><b>EP11 — Gestión de Clientes (Proveedor):</b> Listado y detalle de empresas solicitantes desde la vista del proveedor.</td>
</tr>
<tr>
  <td>US-31</td>
  <td>Ver listado de empresas</td>
  <td>Como proveedor, quiero ver una lista de empresas solicitantes para identificar a mis clientes frecuentes.</td>
  <td><b>Escenario 1: Visualización del listado</b><br/>Dado que el proveedor accede al módulo de empresas,<br/>Cuando se carga el listado,<br/>Entonces se muestran nombre, pedidos activos y total histórico por empresa.<br/><br/><b>Escenario 2: Lista vacía o sin datos</b><br/>Dado que el proveedor accede al módulo y no hay empresas registradas,<br/>Cuando se carga la vista,<br/>Entonces se muestra un mensaje indicando que no hay empresas disponibles.</td>
  <td>EP11</td>
</tr>
<tr>
  <td>US-32</td>
  <td>Ver detalles de empresa</td>
  <td>Como proveedor, quiero ver información detallada de una empresa solicitante para analizar su historial de pedidos.</td>
  <td><b>Escenario 1: Acceso a detalle de empresa</b><br/>Dado que el proveedor selecciona una empresa,<br/>Cuando se carga el detalle,<br/>Entonces visualiza pedidos realizados, cantidades solicitadas y fechas.<br/><br/><b>Escenario 2: Empresa sin historial de pedidos</b><br/>Dado que el proveedor selecciona una empresa que aún no ha realizado pedidos,<br/>Cuando se accede a su perfil,<br/>Entonces se muestra un mensaje indicando que no hay historial disponible.</td>
  <td>EP11</td>
</tr>

<!-- EP12 -->
<tr>
  <td colspan="5"><b>EP12 — Reportes y Analytics:</b> Gráficos de consumo y ventas, y descarga de reportes en PDF para ambos segmentos.</td>
</tr>
<tr>
  <td>US-33</td>
  <td>Ver gráfico de consumo (Solicitante)</td>
  <td>Como solicitante, quiero ver un gráfico de mi consumo mensual para tener control sobre el uso del combustible.</td>
  <td><b>Escenario 1: Gráfico con datos disponibles</b><br/>Dado que el solicitante ha realizado pedidos,<br/>Cuando accede al módulo de reportes,<br/>Entonces se visualiza un gráfico con galones consumidos por mes.<br/><br/><b>Escenario 2: Sin datos de consumo</b><br/>Dado que el solicitante no ha hecho pedidos aún,<br/>Cuando accede al gráfico,<br/>Entonces se muestra un mensaje de que no hay datos suficientes.</td>
  <td>EP12</td>
</tr>
<tr>
  <td>US-34</td>
  <td>Ver gráfico de ventas (Proveedor)</td>
  <td>Como proveedor, quiero ver un gráfico de ventas por mes para monitorear el rendimiento del negocio.</td>
  <td><b>Escenario 1: Datos disponibles para graficar</b><br/>Dado que el proveedor ha despachado pedidos,<br/>Cuando accede al módulo de reportes,<br/>Entonces se visualiza un gráfico con las ventas mensuales totales.<br/><br/><b>Escenario 2: Sin pedidos registrados</b><br/>Dado que el proveedor no ha realizado ventas aún,<br/>Cuando accede al gráfico,<br/>Entonces se muestra un mensaje de que no hay datos suficientes.</td>
  <td>EP12</td>
</tr>
<tr>
  <td>US-35</td>
  <td>Descargar reporte PDF</td>
  <td>Como usuario de ambos segmentos, quiero descargar un resumen de pedidos o ventas en formato PDF para archivarlo o compartirlo.</td>
  <td><b>Escenario 1: Generación de PDF con datos</b><br/>Dado que el usuario solicita la descarga del reporte,<br/>Cuando hay datos en el periodo seleccionado,<br/>Entonces se genera un archivo PDF descargable.<br/><br/><b>Escenario 2: No hay datos en el periodo seleccionado</b><br/>Dado que el usuario no tiene registros en el periodo seleccionado,<br/>Cuando se solicita la descarga,<br/>Entonces el sistema notifica que no hay contenido para exportar.<br/><br/><b>Escenario 3: Falla en la generación del PDF</b><br/>Dado que el usuario solicita la descarga del reporte y ocurre un error en el servidor,<br/>Cuando se procesa la solicitud,<br/>Entonces se muestra un mensaje de error sin afectar la sesión.</td>
  <td>EP12</td>
</tr>

<!-- Technical Stories: EP13 -->
<tr>
  <td colspan="5"><b>EP13 — API de Autenticación:</b> Endpoints del backend para login, logout y recuperación de contraseña.</td>
</tr>
<tr>
  <td>TS-01</td>
  <td>Endpoint: Login</td>
  <td>Como developer, quiero un endpoint para autenticar usuarios.</td>
  <td><b>Escenario 1: Autenticación exitosa</b><br/>Dado que el developer incluye credenciales válidas en el request,<br/>Cuando lo envía al endpoint de autenticación,<br/>Entonces recibe un token JWT y un status 200 como respuesta.<br/><br/><b>Escenario 2: Credenciales inválidas</b><br/>Dado que el developer incluye credenciales incorrectas en el request,<br/>Cuando se procesa la solicitud,<br/>Entonces se retorna status 401 con un mensaje de error.<br/><br/><b>Escenario 3: Error interno del servidor</b><br/>Dado que el developer realiza un request y ocurre un problema en el backend,<br/>Cuando se procesa la autenticación,<br/>Entonces se retorna status 500 con un mensaje genérico de error.</td>
  <td>EP13</td>
</tr>
<tr>
  <td>TS-02</td>
  <td>Endpoint: Recuperar contraseña</td>
  <td>Como developer, quiero un endpoint para que permita enviar correo de recuperación.</td>
  <td><b>Escenario 1: Solicitud válida</b><br/>Dado que el developer envía un request con un correo que existe en la base de datos,<br/>Cuando el request llega al endpoint de recuperación,<br/>Entonces el sistema genera un token y envía el correo de recuperación.<br/><br/><b>Escenario 2: Correo inexistente</b><br/>Dado que el developer envía un request con un correo no registrado,<br/>Cuando se procesa la solicitud,<br/>Entonces se retorna status 404 y no se envía ningún correo.<br/><br/><b>Escenario 3: Error en el envío del correo</b><br/>Dado que el developer ejecuta la acción y ocurre un fallo en el servicio de correo,<br/>Cuando se intenta enviar el mensaje,<br/>Entonces se retorna status 500 y se registra el error en los logs del servidor.</td>
  <td>EP13</td>
</tr>
<tr>
  <td>TS-03</td>
  <td>Endpoint: Logout</td>
  <td>Como developer, quiero un endpoint para cerrar sesión.</td>
  <td><b>Escenario 1: Logout exitoso</b><br/>Dado que el developer envía un token de sesión válido,<br/>Cuando llama al endpoint de logout,<br/>Entonces la sesión se invalida y se retorna status 200.<br/><br/><b>Escenario 2: Token inválido o expirado</b><br/>Dado que el developer incluye un token no válido o expirado,<br/>Cuando se llama al endpoint de logout,<br/>Entonces se retorna status 401 y no se realiza ninguna acción.<br/><br/><b>Escenario 3: Falla del servidor</b><br/>Dado que el developer realiza un request y ocurre un error interno en el servidor,<br/>Cuando se procesa el logout,<br/>Entonces se retorna status 500 con un mensaje genérico.</td>
  <td>EP13</td>
</tr>

<!-- Technical Stories: EP14 -->
<tr>
  <td colspan="5"><b>EP14 — API de Pedidos:</b> Endpoints del backend para crear y consultar pedidos de combustible.</td>
</tr>
<tr>
  <td>TS-04</td>
  <td>Endpoint: Crear pedido</td>
  <td>Como developer, quiero un endpoint para registrar un nuevo pedido de combustible.</td>
  <td><b>Escenario 1: Petición con datos completos</b><br/>Dado que el developer envía una petición con todos los campos requeridos,<br/>Cuando se procesa el POST,<br/>Entonces se retorna status 201 con el ID del nuevo pedido.<br/><br/><b>Escenario 2: Petición incompleta</b><br/>Dado que el developer envía una petición con campos obligatorios faltantes,<br/>Cuando se procesa la solicitud,<br/>Entonces se retorna status 400 con un mensaje de validación.</td>
  <td>EP14</td>
</tr>

<tr>
  <td>TS-05</td>
  <td>Endpoint: Consultar pedidos por usuario</td>
  <td>Como developer, quiero un endpoint para obtener todos los pedidos de un usuario.</td>
  <td><b>Escenario 1: Usuario con pedidos registrados</b><br/>Dado que el usuario tiene pedidos en el sistema,<br/>Cuando se llama al endpoint,<br/>Entonces retorna un array con sus pedidos y status 200.<br/><br/><b>Escenario 2: Usuario sin pedidos</b><br/>Dado que el usuario no ha realizado pedidos,<br/>Cuando se ejecuta la solicitud,<br/>Entonces retorna un array vacío con status 200.</td>
  <td>EP14</td>
</tr>
</tbody></table>

## 3.2 Impact Mapping

En esta sección se detalla el Impact Mapping de la plataforma FullTank, una técnica que permite alinear el desarrollo de software con los objetivos estratégicos del negocio. A través de este mapa, se identifican las metas comerciales SMART (Business Goals), los actores que influyen en ellas, los impactos en sus comportamientos esperados y los entregables (Deliverables) requeridos para materializar dicho valor.

El equipo elaboró el mapa partiendo de tres Business Goals que cumplen con los criterios SMART:
- **Goal 1 (Principal):** Optimizar la gestión y distribución de combustible, alcanzando 300 empresas solicitantes activas y 100 proveedores registrados en el primer año de operación, reduciendo en un 40% los tiempos de gestión de pedidos.
- **Goal 2:** Lograr que el 70% de los proveedores registrados gestionen al menos 10 pedidos mensuales a través de la plataforma durante los primeros 6 meses de operación.
- **Goal 3:** Reducir el tiempo promedio de gestión de pedidos (desde registro hasta despacho) de 48 horas a 24 horas en el 80% de las operaciones, en los primeros 3 meses de uso activo.

A partir de estas metas se incorporaron como Actors/Personas a los User Personas previamente definidos: Carlos Ramírez (empresa solicitante) y Andrea López (proveedora de combustible). Para cada uno se identificaron los Impacts esperados, es decir, cómo se busca cambiar su comportamiento para lograr el objetivo: en el caso de Carlos, la digitalización del registro de pedidos, la reducción de la dependencia de canales informales, el seguimiento en tiempo real y una mejor toma de decisiones basada en datos; en el caso de Andrea, la centralización de pedidos, la optimización de la planificación logística, la mejora en la comunicación con clientes y el uso de métricas para el control operativo.

A partir de estos impactos se definieron los Deliverables que la plataforma FullTank debe ofrecer para generar dichos cambios en los actores. Entre ellos se incluyen el módulo de registro y gestión de pedidos, el sistema de tracking en tiempo real, el panel de control con métricas operativas, la planificación logística automatizada, el historial de pedidos y el sistema de notificaciones y comunicación integrada. Finalmente, en la columna de User Stories se detallaron historias en formato “Como [persona] deseo [acción] para [beneficio]” (por ejemplo, registro de pedidos, consulta de estado, actualización de entregas, coordinación logística y generación de reportes), lo que permite trazar una línea clara desde los objetivos de negocio hasta las funcionalidades del sistema, asegurando la alineación entre Business Goals, Impacts, Deliverables y el desarrollo de la solución.

 <img src="../assets/chapter-3/impactMapping.png" alt="ImpactMapping de los userPersona"/>


## 3.3 Product Backlog

En esta sección se presenta el Product Backlog del proyecto, el cual consolida y prioriza todas las User Stories y Technical Stories identificadas para la plataforma. Las historias están estimadas en Story Points utilizando la escala de Fibonacci y ordenadas de acuerdo con su valor de negocio y dependencias técnicas para guiar el desarrollo de los futuros sprints.

<table border="1" cellspacing="0" cellpadding="6">
  <thead>
    <tr>
      <th>#Orden</th>
      <th>ID</th>
      <th>Título</th>
      <th>Descripción</th>
      <th>Story Points</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>01</td>
      <td>US-01</td>
      <td>Ver sección Home</td>
      <td>Como visitante (proveedor), quiero ver una sección de inicio que resuma el valor de FullTank para comprender rápidamente el objetivo del sistema.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>02</td>
      <td>US-02</td>
      <td>Ver sección About Us</td>
      <td>Como visitante de ambos segmentos, quiero conocer quiénes están detrás de FullTank para confiar en el sistema.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>03</td>
      <td>US-03</td>
      <td>Ver sección How it works?</td>
      <td>Como visitante de ambos segmentos, quiero entender cómo funciona FullTank paso a paso para evaluar si se ajusta a mis necesidades.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>04</td>
      <td>US-04</td>
      <td>Enviar mensaje de contacto</td>
      <td>Como visitante de ambos segmentos, quiero enviar un mensaje desde Contact Us para solicitar más información.</td>
      <td>5</td>
    </tr>
    <tr>
      <td>05</td>
      <td>US-36</td>
      <td>Ver sección Benefits</td>
      <td>Como visitante de ambos segmentos, quiero conocer las principales ventajas con las que puedo contar para evaluar la implementación de la plataforma.</td>
      <td>1</td>
    </tr>
    <tr>
      <td>06</td>
      <td>US-37</td>
      <td>Ver sección Testimonios de Clientes</td>
      <td>Como visitante de ambos segmentos, quiero conocer los testimonios de los usuarios de FullTank para tener confianza en la plataforma y saber que otras empresas ya la están usando.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>07</td>
      <td>US-38</td>
      <td>Ver sección Planes y Precios</td>
      <td>Como visitante (ambos segmentos), quiero saber qué planes se adecuan a mis necesidades para poder iniciar un proceso de registro o solicitud.</td>
      <td>5</td>
    </tr>
    <tr>
      <td>08</td>
      <td>US-39</td>
      <td>Cambiar idioma de la plataforma</td>
      <td>Como visitante de ambos segmentos, quiero poder cambiar entre inglés y español para entender la plataforma en mi idioma preferido.</td>
      <td>8</td>
    </tr>
    <tr>
      <td>09</td>
      <td>US-05</td>
      <td>Registrar nuevo pedido</td>
      <td>Como solicitante, quiero registrar un pedido con tipo y cantidad de combustible para que el proveedor lo procese.</td>
      <td>5</td>
    </tr>
    <tr>
      <td>10</td>
      <td>US-06</td>
      <td>Consultar estado del pedido</td>
      <td>Como solicitante, quiero ver el estado de mis pedidos para saber si están aprobados, en tránsito o entregados.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>11</td>
      <td>US-07</td>
      <td>Confirmar recepción de pedido</td>
      <td>Como solicitante, quiero confirmar que recibí el pedido para que el proveedor lo cierre.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>12</td>
      <td>US-08</td>
      <td>Registrar información de pago</td>
      <td>Como solicitante, quiero ingresar la información de los pagos correspondientes para validar el pedido ante el proveedor.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>13</td>
      <td>US-09</td>
      <td>Ver historial de pedidos</td>
      <td>Como solicitante, quiero ver mis pedidos anteriores para tener control sobre mi consumo.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>14</td>
      <td>US-10</td>
      <td>Ver pedidos pendientes</td>
      <td>Como proveedor, quiero ver todos los pedidos pendientes para analizarlos y tomar acción.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>15</td>
      <td>US-11</td>
      <td>Aprobar pedido</td>
      <td>Como proveedor, quiero aprobar pedidos según los depósitos hechos a mis cuentas bancarias.</td>
      <td>5</td>
    </tr>
    <tr>
      <td>16</td>
      <td>US-12</td>
      <td>Marcar pedido como despachado</td>
      <td>Como proveedor, quiero marcar cuándo un pedido sale a entrega para notificar al cliente.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>17</td>
      <td>US-13</td>
      <td>Cerrar pedido</td>
      <td>Como proveedor, quiero cerrar el pedido cuando el cliente confirme la entrega para finalizar el proceso.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>18</td>
      <td>US-18</td>
      <td>Ver resumen de pedidos (Solicitante)</td>
      <td>Como solicitante, quiero ver un resumen de mis pedidos para identificar cuántos están en proceso o completados.</td>
      <td>5</td>
    </tr>
    <tr>
      <td>19</td>
      <td>US-19</td>
      <td>Ver resumen de pedidos (Proveedor)</td>
      <td>Como proveedor, quiero ver un resumen de pedidos gestionados y pendientes para organizar a los clientes.</td>
      <td>5</td>
    </tr>
    <tr>
      <td>20</td>
      <td>US-40</td>
      <td>Registrar empresa solicitante</td>
      <td>Como visitante (solicitante), quiero registrar mi empresa en la plataforma para comenzar a realizar pedidos de combustible.</td>
      <td>5</td>
    </tr>
    <tr>
      <td>21</td>
      <td>US-41</td>
      <td>Registrar empresa proveedora</td>
      <td>Como visitante (proveedor), quiero registrar mi empresa distribuidora en la plataforma para comenzar a gestionar pedidos de combustible.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>22</td>
      <td>US-43</td>
      <td>Ver detalle de pedido</td>
      <td>Como usuario de ambos segmentos, quiero ver el detalle completo de un pedido para revisar toda la información asociada.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>23</td>
      <td>US-42</td>
      <td>Rechazar pedido</td>
      <td>Como proveedor, quiero rechazar un pedido cuando no pueda atenderlo para notificar al solicitante oportunamente.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>24</td>
      <td>US-20</td>
      <td>Asignar vehículo a pedido</td>
      <td>Como proveedor, quiero asignar un vehículo a un pedido aprobado para organizar la logística.</td>
      <td>5</td>
    </tr>
    <tr>
      <td>25</td>
      <td>US-21</td>
      <td>Asignar conductor a pedido</td>
      <td>Como proveedor, quiero asignar un conductor para completar la información de despacho.</td>
      <td>5</td>
    </tr>
    <tr>
      <td>26</td>
      <td>US-22</td>
      <td>Validar disponibilidad de transporte</td>
      <td>Como proveedor, quiero saber qué vehículos están disponibles antes de asignarlos para vincularlos correctamente.</td>
      <td>8</td>
    </tr>
    <tr>
      <td>27</td>
      <td>US-44</td>
      <td>Gestionar vehículos de flota</td>
      <td>Como proveedor, quiero registrar y administrar los vehículos de mi flota para tenerlos disponibles al momento de asignarlos a pedidos.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>28</td>
      <td>US-45</td>
      <td>Gestionar conductores</td>
      <td>Como proveedor, quiero registrar y administrar los conductores de mi empresa para asignarlos correctamente a los despachos.</td>
      <td>5</td>
    </tr>
    <tr>
      <td>29</td>
      <td>US-23</td>
      <td>Ver perfil de usuario</td>
      <td>Como usuario registrado, quiero ver mis datos de perfil para revisar mi información registrada.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>30</td>
      <td>US-24</td>
      <td>Editar datos de perfil</td>
      <td>Como usuario registrado, quiero editar mis datos para mantener mi información actualizada.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>31</td>
      <td>US-33</td>
      <td>Ver gráfico de consumo (Solicitante)</td>
      <td>Como solicitante, quiero ver un gráfico de mi consumo mensual para tener control sobre el uso del combustible.</td>
      <td>5</td>
    </tr>
    <tr>
      <td>32</td>
      <td>US-34</td>
      <td>Ver gráfico de ventas (Proveedor)</td>
      <td>Como proveedor, quiero ver un gráfico de ventas por mes para monitorear el rendimiento del negocio.</td>
      <td>5</td>
    </tr>
    <tr>
      <td>33</td>
      <td>US-35</td>
      <td>Descargar reporte PDF</td>
      <td>Como usuario de ambos segmentos, quiero descargar un resumen de pedidos o ventas en formato PDF para archivarlo o compartirlo.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>34</td>
      <td>US-14</td>
      <td>Generar reporte de ventas</td>
      <td>Como proveedor, quiero generar reportes de ventas para tener registro de operaciones realizadas.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>35</td>
      <td>US-27</td>
      <td>Buscar pedido por código</td>
      <td>Como usuario de ambos segmentos, quiero buscar un pedido específico por su código para encontrarlo rápidamente.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>36</td>
      <td>US-28</td>
      <td>Filtrar pedidos por estado</td>
      <td>Como usuario de ambos segmentos, quiero filtrar mis pedidos por estado (pendiente, aprobado, entregado) para facilitar la revisión.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>37</td>
      <td>US-29</td>
      <td>Recibir notificación de aprobación</td>
      <td>Como solicitante, quiero recibir una notificación cuando un pedido sea aprobado o rechazado para estar informado.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>38</td>
      <td>US-30</td>
      <td>Notificación de pedido despachado</td>
      <td>Como solicitante, quiero recibir una notificación cuando un pedido haya sido despachado para estar informado.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>39</td>
      <td>US-31</td>
      <td>Ver listado de empresas</td>
      <td>Como proveedor, quiero ver una lista de empresas solicitantes para identificar a mis clientes frecuentes.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>40</td>
      <td>US-32</td>
      <td>Ver detalles de empresa</td>
      <td>Como proveedor, quiero ver información detallada de una empresa solicitante para analizar su historial de pedidos.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>41</td>
      <td>US-25</td>
      <td>Ver sección de preguntas frecuentes</td>
      <td>Como visitante de ambos segmentos, quiero acceder a una sección de preguntas frecuentes para resolver dudas rápidamente.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>42</td>
      <td>US-26</td>
      <td>Acceder a información de contacto rápido</td>
      <td>Como usuario de ambos segmentos, quiero ver datos de contacto directo (teléfono o correo) para hacer consultas urgentes.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>43</td>
      <td>US-15</td>
      <td>Iniciar sesión</td>
      <td>Como usuario registrado, quiero iniciar sesión con correo y contraseña para acceder a mi cuenta.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>44</td>
      <td>US-16</td>
      <td>Recuperar contraseña</td>
      <td>Como usuario registrado, quiero recuperar mi contraseña para volver a acceder si la olvidé.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>45</td>
      <td>US-17</td>
      <td>Cerrar sesión</td>
      <td>Como usuario registrado, quiero poder cerrar sesión para mantener segura mi cuenta.</td>
      <td>1</td>
    </tr>
    <tr>
      <td>46</td>
      <td>TS-01</td>
      <td>Endpoint: Login</td>
      <td>Como developer, quiero un endpoint para autenticar usuarios.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>47</td>
      <td>TS-02</td>
      <td>Endpoint: Recuperar contraseña</td>
      <td>Como developer, quiero un endpoint para que permita enviar correo de recuperación.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>48</td>
      <td>TS-03</td>
      <td>Endpoint: Logout</td>
      <td>Como developer, quiero un endpoint para cerrar sesión.</td>
      <td>2</td>
    </tr>
    <tr>
      <td>49</td>
      <td>TS-04</td>
      <td>Endpoint: Crear pedido</td>
      <td>Como developer, quiero un endpoint para registrar un nuevo pedido de combustible.</td>
      <td>3</td>
    </tr>
    <tr>
      <td>50</td>
      <td>TS-05</td>
      <td>Endpoint: Consultar pedidos por usuario</td>
      <td>Como developer, quiero un endpoint para obtener todos los pedidos de un usuario.</td>
      <td>3</td>
    </tr>
  </tbody>
</table>

Link del Trello: https://trello.com/b/69e2fd01ee5b055b2d967a45/fulltank

![alt text](../assets/chapter-3/trello.png)
