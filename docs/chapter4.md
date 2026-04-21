# Capítulo IV: Product Design

## 4.1 Style Guidelines
En esta sección el equipo presenta la Guía de Estilos de Full-Tank.
### 4.1.1 General Style Guidelines
En esta sección se definen los aspectos visuales y comunicativos que garantizan una experiencia consistente en todos los puntos de contacto de la solución Full-Tank. Nuestras decisiones de diseño se basan en los principios de Material Design, adaptándolos para transmitir confianza, eficiencia y modernidad en el sector energético.

**Branding**

El logotipo de Full-Tank es el eje central de nuestra identidad.

- **Concepto:** La integración de las iniciales "FT" con un indicador circular (que evoca tanto un reloj como un manómetro de combustible) simboliza los dos pilares de nuestra propuesta de valor: precisión operativa y trazabilidad en tiempo real.
  
- **Identidad Visual:** El diseño utiliza líneas geométricas sólidas para transmitir robustez y confiabilidad, características esenciales para un sistema que gestiona recursos críticos en sectores como minería y construcción.
  
<div align="center">
  <img src="./../assets/chapter-4/logo_FullTank.png" alt="Logo FullTank" width="310"/>
</div>


**Typography**

Se ha seleccionado la familia tipográfica Inter para toda la plataforma.

- **Sustento:** Inter es una fuente sans-serif diseñada específicamente para pantallas de computadoras. Su alta legibilidad en tamaños pequeños es crucial para los tableros de control (dashboards) donde los usuarios deben leer cifras y estados de pedidos rápidamente sin fatiga visual.

- **Jerarquía Tipográfica:** 
  - **Headlines (Inter Bold):** Se utiliza para títulos de sección y métricas clave (KPIs), estableciendo una jerarquía visual clara.
  - **Body (Inter Regular):** Para descripciones, tablas de datos e información general.
  - **Labels (Inter Medium):** Para etiquetas de formularios y metadatos, diferenciándose sutilmente del texto de cuerpo.


**Colors**

Nuestra paleta de colores equilibra el profesionalismo corporativo con la identidad del sector energético:

- **Primary (#1E3A8A):** Un azul profundo que transmite seguridad, confianza y autoridad. Es el color base para la navegación y acciones principales, alineado al perfil B2B de la startup.
- **Secondary (#6D7698):** Un tono pizarra que aporta estabilidad visual y se utiliza en elementos de soporte para no saturar al usuario.
- **Tertiary/Accent (#F59E0B):** El color del "combustible" y la energía. Se utiliza estratégicamente para botones de acción (Call to Action), alertas críticas y estados que requieren atención inmediata.
- **Neutral (#475569):** Utilizado para textos secundarios y fondos, garantizando un contraste adecuado para la accesibilidad.
  

**Estilos**
<div align="center">
  <img src="./../assets/chapter-4/estilo.png" alt="Estilos" width="310"/>
</div>

**Spacing**

Siguiendo los lineamientos de Material Design, implementamos un sistema de rejilla basado en una unidad base de 8dp.

- **Decisión:** Todos los márgenes, rellenos (padding) y dimensiones de componentes son múltiplos de 8. Esto asegura que la interfaz sea adaptable (responsive) y que los elementos tengan "aire" suficiente, reduciendo la carga cognitiva de los operadores logísticos que manejan múltiples pedidos simultáneamente.
  

**Tone of Voice and Language**

Dado que interactuamos con gerentes de logística y proveedores industriales, el tono de Full-Tank se define en las siguientes dimensiones:

- **Serio:** El manejo de combustibles implica altos costos y riesgos; la comunicación debe ser precisa y técnica.
- **Formal:** Mantenemos un estándar corporativo para generar respeto y profesionalismo entre empresas (B2B).
- **Respetuoso:** Las notificaciones y mensajes de error son constructivos y amables, evitando tecnicismos innecesarios que confundan al usuario.
- **Sereno:** Buscamos transmitir calma y control, especialmente en situaciones de retrasos logísticos, mediante interfaces limpias y mensajes directos.

### 4.1.2 Web Style Guidelines
Esta sección detalla los estándares de diseño de interfaz y comportamiento de interacción para la plataforma web de Full-Tank, asegurando una experiencia fluida tanto en navegadores de escritorio como en dispositivos móviles.

**1. Grid and Breakpoints**
  - Para garantizar que la interfaz sea responsive, adoptamos el sistema de rejilla de Material Design basado en columnas:

  - **Desktop (1200px)**: Layout de 12 columnas con márgenes laterales de 24dp.

  - **Mobile (360px - 599px)**: Layout de 4 columnas, donde los elementos se apilan verticalmente para facilitar el scroll con una sola mano.

  - **Spacing**: Se mantiene la unidad base de 8dp para todos los componentes, asegurando consistencia visual en cualquier resolución.
  
**2. UI Components (Angular Material)**

Se utiliza la biblioteca de componentes de Angular Material para estandarizar la interacción:

- **Buttons:** Los botones principales (como Create Order) utilizan el estilo mat-raised-button con nuestro color primario (#1E3A8A). Los botones de advertencia o acciones secundarias utilizan mat-stroked-button.

- **Form Fields:** Los campos de entrada de datos emplean el estilo "Outline" para mejorar la legibilidad en entornos industriales, incluyendo iconos descriptivos para guiar al usuario.

- **Cards:** La información de los pedidos se organiza en mat-card para separar visualmente cada transacción y permitir una lectura rápida.

**3. Interaction States and Feedback**

Los estándares de interacción definen cómo responde el sistema a las acciones del usuario:

- **Hover States:** En la versión Desktop, los elementos interactuables (botones, filas de tabla) cambian su elevación o tono de color ligeramente al pasar el cursor, indicando que son clickeables.

- **Active/Focus States:** Siguiendo las guías de accesibilidad, cada elemento enfocado mediante el teclado tendrá un anillo de enfoque claro.

- **Loading States:** Durante la carga de datos masivos de combustible, se utilizarán mat-progress-spinner o skeletons para informar al usuario que el proceso está en curso.

**4. Responsive Navigation**

- **Desktop:** Se utiliza un Sidebar (menú lateral) fijo para acceso rápido a Dashboard, Orders, e History.

- **Mobile:** El Sidebar se oculta automáticamente y es accesible a través de un "hamburger menu" en la parte superior izquierda, maximizando el espacio para la visualización de datos críticos.


## 4.2 Information Architecture

Esta sección describe los aspectos clave de la estructura y el etiquetado del aplicativo.

### 4.2.1 Organization Systems
### 4.2.2 Labeling Systems
En Full-Tank, el sistema de etiquetado ha sido diseñado priorizando la simplicidad y la reducción de la carga cognitiva de los operadores logísticos y proveedores. Se han seleccionado etiquetas descriptivas de una o dos palabras para evitar confusión y agilizar la navegación.

1. **Landing Page Labels**
Las etiquetas del sitio web estático buscan guiar al visitante rápidamente hacia la propuesta de valor y la conversión:

- **Home**: Representa la página principal y el resumen de la propuesta de valor.

- **About Us**: Agrupa la información sobre la misión, visión y el equipo detrás de Prime Fuel.

- **Frecuency Asked Questions**: Agrupa las preguntas frecuentes sobre el servicio.

- **Pricing**: Agrupa los planes de suscripción y costos del servicio SaaS.

- **Contact Us**: Indica el espacio para canales de comunicación directa (correo, teléfono).
  
2. **Web Application Labels (Dashboard & Navigation)**
Las etiquetas dentro de la aplicación están diseñadas para que perfiles como Carlos o Andrea encuentren las funcionalidades operativas sin esfuerzo:

- **Dashboard**: Representa el panel principal con los KPIs y métricas clave resumidas.

- **Orders**: Etiqueta general que agrupa tanto el historial como la creación de nuevos pedidos de combustible.

- **Fleet / Vehicles**: Agrupa la gestión de las cisternas y conductores asignados para los despachos.

- **Reports**: Asocia las funcionalidades de descarga de documentos en PDF, gráficos de consumo y análisis de ventas.

- **Settings**: Representa las configuraciones de perfil de usuario, seguridad y preferencias de la cuenta.

3. **Status Labels (Estados de Pedido)**
Para evitar confusiones en el seguimiento en tiempo real, se estandarizan las siguientes etiquetas de estado:

- **Pending**: Pedido creado pero aún no revisado/aprobado por el proveedor.

- **Approved**: Pagos validados y pedido aceptado.

- **In Transit**: El vehículo con el combustible ha sido despachado.

- **Completed**: El cliente ha confirmado la recepción satisfactoria del combustible.

### 4.2.3 SEO Tags and Meta Tags
### 4.2.4 Searching Systems
### 4.2.5 Navigation Systems

## 4.3 Landing Page UI Design
### 4.3.1 Landing Page Wireframe
### 4.3.2 Landing Page Mock-up

## 4.4 Web Applications UX/UI Design
### 4.4.1 Web Applications Wireframes
### 4.4.2 Web Applications Wireflow Diagrams
### 4.4.3 Web Applications Mock-ups
### 4.4.4 Web Applications User Flow Diagrams

User Goal 1: El usuario registrado desea iniciar sesión en la aplicación para acceder a su cuenta y gestionar sus pedidos de combustible.

User Personas: Solicitante / Proveedor.

Happy Path
En esta ruta esperada, el usuario ya cuenta con un registro previo en el sistema. El flujo inicia cuando el usuario se encuentra en la pantalla de "Login". Al ingresar sus credenciales válidas (correo electrónico y contraseña) y hacer clic en el botón de iniciar sesión, el sistema autentica los datos y redirige al usuario exitosamente a la vista principal (Dashboard), dándole acceso completo a las funciones de su rol.

Unhappy Paths
Estas rutas alternas contemplan los escenarios donde el usuario no logra autenticarse debido a errores en el ingreso de datos. Puede ocurrir que el usuario ingrese una contraseña incorrecta, un correo no registrado, o que intente enviar el formulario con campos vacíos. En estos casos, el flujo se interrumpe y el sistema se mantiene en la vista actual, mostrando un mensaje de validación o alerta visual para que el usuario corrija la información.

User Goal 2: El visitante desea crear una cuenta nueva en la plataforma para poder acceder a los servicios como solicitante o proveedor de combustible.

User Personas: Visitante (Futuro Solicitante / Futuro Proveedor).

Happy Path
En esta ruta esperada, el flujo se centra en el proceso de creación de una cuenta nueva. El usuario inicia en la pantalla de "Registro" (a la cual puede llegar desde la página de Inicio o desde la vista de Login). El usuario completa todos los campos requeridos del formulario (por ejemplo: nombre, correo electrónico, contraseña y selección de rol: Solicitante o Proveedor). Al hacer clic en el botón "Registrarse", el sistema valida que los datos sean correctos, crea la cuenta de forma exitosa y redirige al usuario a su respectivo Dashboard de bienvenida (o a la pantalla de Inicio de Sesión para confirmar sus credenciales).

Unhappy Paths
Estas rutas alternas toman en cuenta los escenarios donde el usuario ingresa información que no pasa las verificaciones del sistema o no completa los espacios obligatorios. Los errores más comunes incluyen: intentar registrar un correo electrónico que ya existe en la base de datos, ingresar contraseñas que no coinciden en el campo de confirmación, o dejar campos vitales en blanco. En estos casos, la creación de la cuenta se bloquea y el usuario permanece en la pantalla de Registro, donde el sistema despliega alertas visuales o mensajes de error específicos debajo de cada campo afectado para que pueda corregirlos.

User Goal 3: El usuario registrado desea recuperar el acceso a su cuenta solicitando un enlace para cambiar su contraseña olvidada.

User Personas: Usuario Registrado (Solicitante / Proveedor).

Happy Path
En esta ruta esperada, el flujo inicia cuando el usuario, al no poder acceder a su cuenta, selecciona la opción "¿Olvidaste tu contraseña?" en la pantalla de Inicio de Sesión. Esto lo redirige a la vista de Recuperación, donde debe ingresar el correo electrónico asociado a su cuenta. Al presionar el botón de enviar, el sistema valida el correo y muestra un mensaje confirmando el envío de un enlace de recuperación. El usuario interactúa con dicho enlace (simulado en el flujo) y es dirigido a la pantalla de "Restablecer Contraseña", donde ingresa su nueva contraseña y la confirma. Al guardar, el sistema actualiza las credenciales exitosamente y redirige al usuario de vuelta al Login.

Unhappy Paths
Estas rutas alternas contemplan los fallos de validación en dos momentos distintos del proceso. El primer escenario ocurre si el usuario ingresa un correo electrónico que no existe en la base de datos o si deja el campo en blanco; en este caso, el sistema bloquea el envío del correo y muestra un mensaje de error indicando que la cuenta no está registrada. El segundo escenario de error se da en la pantalla de restablecimiento: si el usuario digita una nueva contraseña pero falla al confirmarla (los campos no coinciden) o no cumple con los caracteres mínimos requeridos, el botón de guardado se deshabilita o el sistema arroja una alerta visual solicitando la corrección antes de proceder.

User Goal 4: El usuario desea registrar un nuevo pedido especificando el tipo y la cantidad de combustible para que el proveedor lo procese.

User Persona: Solicitante.

Happy Path
En esta ruta esperada, el flujo representa la funcionalidad principal del sistema. El usuario (Solicitante), habiendo iniciado sesión, se encuentra en su Dashboard o panel principal. Desde allí, selecciona la opción para "Crear Nuevo Pedido". El sistema le presenta un formulario donde ingresa los datos requeridos (tipo de combustible, cantidad en galones, y dirección o tanque de destino). Al completar correctamente la información y hacer clic en "Enviar Pedido" (o "Registrar"), el sistema procesa la solicitud, la guarda en la base de datos con un estado inicial de "Pendiente" y redirige al usuario a una pantalla de confirmación de éxito o al listado de sus pedidos recientes.

Unhappy Paths
Estas rutas alternas ocurren cuando el usuario comete errores al intentar registrar su solicitud de combustible, lo que impide que el pedido se envíe al proveedor. Esto puede suceder si el usuario deja campos obligatorios vacíos (como olvidar seleccionar el tipo de combustible) o si ingresa valores inválidos (por ejemplo, una cantidad de galones igual o menor a cero, o que exceda el límite permitido por el sistema). Al intentar enviar el formulario con estas inconsistencias, el sistema bloquea la acción, permanece en la vista del formulario y resalta los campos afectados con mensajes de advertencia, indicando al usuario que debe corregir las cantidades o completar la información para poder continuar.

User Goal 5: El usuario proveedor desea revisar un pedido pendiente y aprobarlo tras validar que los depósitos realizados a sus cuentas bancarias cubren el monto total.

User Persona: Proveedor.

Happy Path
En esta ruta esperada, el flujo se ejecuta desde la perspectiva de la administración del negocio. El usuario (Proveedor) inicia en su Dashboard y accede a la sección de "Pedidos Pendientes". Selecciona un pedido específico de la lista para acceder a sus detalles completos. Allí, el proveedor verifica que el solicitante haya registrado correctamente la información del pago y que los depósitos cubran el costo total del combustible solicitado. Al validar esta información, el usuario presiona el botón "Aprobar Pedido". El sistema procesa la acción, cambia el estado del pedido a "Aprobado" y muestra una notificación de éxito, devolviendo al usuario al listado actualizado.

Unhappy Paths
Estas rutas alternas se presentan cuando las condiciones financieras del pedido no se cumplen. El proveedor revisa los detalles del pedido, pero identifica que los depósitos registrados por el solicitante son inválidos, inexistentes o el monto ingresado es insuficiente para cubrir la totalidad del pedido. Si el proveedor intenta hacer clic en "Aprobar" bajo estas condiciones (o selecciona una opción explícita de "Rechazar/Observar"), el sistema bloquea el cambio a estado "Aprobado". En su lugar, se despliega una alerta visual o un mensaje de error indicando que el pedido no cuenta con el pago completo, manteniendo el estado en pendiente o pausado hasta que el cliente regularice la situación.

## 4.5 Web Applications Prototyping

## 4.6 Domain-Driven Software Architecture
### 4.6.1 Design-Level Event Storming
### 4.6.2 Software Architecture Context Diagram
### 4.6.3 Software Architecture Container Diagrams
### 4.6.4 Software Architecture Components Diagrams

## 4.7 Software Object-Oriented Design
### 4.7.1 Class Diagrams

## 4.8 Database Design
### 4.8.1 Database Diagrams