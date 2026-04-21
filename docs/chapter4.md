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
En esta sección se presentan los esquemas estructurales (wireframes) de baja fidelidad para la Landing Page de *Full-Tank*, diseñados en Figma. Estos diagramas establecen la jerarquía visual, la distribución de contenido y el comportamiento responsivo antes de aplicar el estilo visual final, asegurando que la interfaz cumpla con nuestros objetivos de negocio.

**Desktop Web Browser Wireframe**
<div align="center">
  <img src="./../assets/chapter-4/landingPage_wireframe.png" alt="Wireframe" width="100%"/>
</div>

* **Header (Navegación):** Se utiliza una organización horizontal fija con el logotipo a la izquierda, los enlaces de navegación centralizados (*Home, How it works, Benefits, Pricing, Testimonials, Contact) y el botón principal de *Call to Action (*"Request a Demo"*) resaltado a la derecha para incentivar la conversión inmediata.
* **Hero Section (Home):** Ocupa la primera vista con un título de propuesta de valor centrado, un subtítulo descriptivo y un botón primario de "Request a Demo", acompañado de un placeholder (caja gris) para una imagen representativa del dashboard de TankMaster a la derecha.
* **Body Sections:**
    * **How it works:** Se organiza secuencialmente en 3 o 4 columnas, mostrando los pasos del flujo operativo.
    * **Benefits & Testimonials:** Se estructuran de forma matricial para facilitar la lectura de características clave y generar confianza al mostrar los casos de éxito de otras empresas.
    * **Pricing:** Presentado mediante tablas comparativas para destacar claramente los planes de suscripción.
* **Footer:** Contiene los enlaces legales obligatorios (Términos y Condiciones), información de contacto y enlaces a redes sociales, cumpliendo con la ética y responsabilidad exigida en el proyecto.


### 4.3.2 Landing Page Mock-up

## 4.4 Web Applications UX/UI Design

Los wireframes y mockups aquí presentados muestran la estructura inicial de las vistas principales, priorizando la jerarquía visual, la simplicidad de navegación, la accesibilidad, la escalabilidad futura y la claridad en la presentación de información crítica como rutas, paraderos, notificaciones y configuraciones del usuario.

### 4.4.1 Web Applications Wireframes

Esta sección presenta la propuesta visual y funcional de las aplicaciones que integran la experiencia de FullTank, diseñada para optimizar la interacción entre proveedores y compradores de combustible.

**Wireframe 1 / Inicial**

El primer wireframe representa la Landing Page principal de FullTank, diseñada como una herramienta de conversión masiva para atraer tanto a empresas solicitantes como a proveedores.

En el cuerpo de la página, la información se desglosa siguiendo una secuencia lógica que construye confianza y educación sobre el servicio. Se incluyen secciones dedicadas a la historia de la startup (About Us) y al funcionamiento paso a paso del sistema (How it works), utilizando bloques modulares que permiten un escaneo rápido del contenido. Esta estructura se complementa con una cuadrícula de características que resaltan los beneficios técnicos, como la trazabilidad y la centralización de datos, fundamentales para resolver los dolores detectados en la etapa de investigación.

Hacia el final de la navegación, se presenta una sección de planes y suscripciones que utiliza el principio de jerarquía visual para destacar la opción más equilibrada, facilitando la toma de decisiones del usuario. El diseño concluye con un pie de página (footer) que centraliza los datos de contacto y redes sociales, asegurando que el usuario tenga siempre una vía de comunicación abierta con TechnoSAC. Todo el conjunto ha sido diseñado bajo criterios de diseño inclusivo, empleando dimensiones de botones generosas y una organización de elementos que prioriza la legibilidad y la facilidad de interacción en dispositivos móviles.

<div align="center">
  <img src="./../assets/chapter-4/Wireframe1.png" alt="Estilos" width="310"/>
</div>

**Wireframe 2**

El wireframe de Inicio de Sesión y Registro establece un punto de control centralizado diseñado para identificar al usuario y derivarlo de manera eficiente a su panel de control correspondiente. La arquitectura de información prioriza la funcionalidad sobre cualquier otro elemento, disponiendo de forma secuencial los campos de captura de credenciales, el acceso a la recuperación de cuenta y el disparador para la creación de nuevos perfiles. Este esquema garantiza que el usuario recorra el camino mínimo necesario para la autenticación, reduciendo la carga cognitiva al segmentar claramente las acciones primarias de las secundarias.

<div align="center">
  <img src="./../assets/chapter-4/Inicio.png" alt="Estilos" width="700"/>
</div>

**Wireframe 3**

El primer wireframe para proveedores, denominado Resumen Operativo, establece una arquitectura de información de alta prioridad que condensa la salud del negocio en tres indicadores clave: ventas mensuales, pedidos pendientes y vehículos en ruta.

<div align="center">
  <img src="./../assets/chapter-4/Wireframe2.png" alt="Estilos" width="700"/>
</div>

**Wireframe 4**

El wireframe de Gestión de Pedidos Entrantes estructura la información mediante una tabla funcional que centraliza las solicitudes nuevas, permitiendo al proveedor procesar múltiples órdenes desde una sola vista. La arquitectura de información se organiza en columnas que detallan datos críticos como el cliente, el tipo de combustible y la cantidad, situando los botones de acción en el extremo derecho para facilitar una respuesta rápida de aprobación o rechazo.

<div align="center">
  <img src="./../assets/chapter-4/Wireframe3.png" alt="Estilos" width="700"/>
</div>

**Wireframe 5**

El wireframe de Directorio de Clientes utiliza un sistema de tarjetas (cards) para organizar el perfil detallado de cada empresa, permitiendo al proveedor acceder a la información de contacto y preferencias de compra de manera individualizada. La arquitectura de información se segmenta visualmente mediante el uso de listas de verificación e iconos, lo que facilita el escaneo rápido de los servicios contratados o requisitos específicos por cliente.

<div align="center">
  <img src="./../assets/chapter-4/Wireframe4.png" alt="Estilos" width="700"/>
</div>

**Wireframe 6**

El wireframe de Asignación de Despacho presenta una arquitectura de información dividida en dos paneles estratégicos para facilitar la coordinación logística del proveedor. El panel izquierdo concentra los campos de entrada para la selección de pedidos y la vinculación de unidades de transporte, incluyendo un contenedor específico para la validación de documentos o firmas digitales, lo que asegura que cada despacho cumpla con los requisitos administrativos.

<div align="center">
  <img src="./../assets/chapter-4/Wireframe5.png" alt="Estilos" width="700"/>
</div>

**Wireframe 7**

El wireframe de Reportes y Documentación cierra el panel de proveedores con una arquitectura de información orientada a la auditoría y el control administrativo. La interfaz dispone de un área central de visualización para previsualizar registros operativos, acompañada de un botón de acción principal para la generación y descarga de documentos legales o reportes de ventas.

<div align="center">
  <img src="./../assets/chapter-4/Wireframe6.png" alt="Estilos" width="700"/>
</div>

**Wireframe 8**

El primer wireframe del panel de Compradores introduce la vista de Consumo General, diseñada para ofrecer una arquitectura de información centrada en el control financiero y operativo del solicitante. La interfaz utiliza una disposición horizontal de tres tarjetas de métricas que permiten al usuario monitorear, de forma inmediata, su gasto total mensual, el volumen de consumo acumulado y la cantidad de pedidos que se encuentran actualmente en estado pendiente.

<div align="center">
  <img src="./../assets/chapter-4/Wireframe7.png" alt="Estilos" width="700"/>
</div>

**Wireframe 9**

El wireframe de Solicitud de Combustible y Procedimiento de Pago funciona como una interfaz de formulario estructurada para guiar al comprador a través del registro de una nueva orden. La arquitectura de información divide el proceso en dos bloques lógicos: la especificación técnica del pedido (tipo de combustible y cantidad) y la carga de la evidencia de pago necesaria para la validación del proveedor. Al presentar los campos de manera simétrica y clara dentro de un contenedor enfocado, se minimiza el riesgo de errores en el ingreso de datos, asegurando que el flujo desde la solicitud hasta la confirmación del depósito sea fluido y cumpla con los requisitos operativos del sistema.

<div align="center">
  <img src="./../assets/chapter-4/Wireframe8.png" alt="Estilos" width="700"/>
</div>

**Wireframe 10**

El wireframe de Seguimiento del Pedido se centra en proporcionar transparencia y tranquilidad al comprador mediante una arquitectura de información que destaca el progreso del suministro en tiempo real. El elemento principal de esta interfaz es una barra de estado dinámica que permite visualizar de forma gráfica en qué etapa se encuentra el pedido (solicitado, aprobado, en tránsito o entregado), eliminando la incertidumbre del usuario. 

<div align="center">
  <img src="./../assets/chapter-4/Wireframe9.png" alt="Estilos" width="700"/>
</div>

**Wireframe 11**

El wireframe del Historial de Pedidos cierra la experiencia del comprador mediante una arquitectura de información que facilita la consulta de transacciones pasadas para fines de auditoría y control de inventarios. La interfaz organiza los pedidos anteriores en una cuadrícula de tarjetas (cards), donde cada una presenta un resumen de la transacción, incluyendo fechas y volúmenes, acompañada de un botón de acción para acceder a detalles específicos o descargar comprobantes.

<div align="center">
  <img src="./../assets/chapter-4/Wireframe10.png" alt="Estilos" width="700"/>
</div>


### **Mobile**
**Wireframe 1**

La adaptación móvil de la página principal prioriza la jerarquía vertical para asegurar una navegación fluida en pantallas pequeñas. La arquitectura de información reorganiza el menú en un componente de "hamburguesa" y transforma las tarjetas de planes y beneficios en una disposición de columna única. Los botones de llamado a la acción se han redimensionado para ocupar el ancho de la pantalla, facilitando la interacción táctil y guiando al usuario directamente hacia el registro o inicio de sesión.

<div align="center">
  <img src="./../assets/chapter-4/Prinicpial Mobile.png" alt="Estilos" width="200"/>
</div>

**Wireframe 2**

Los wireframes de Inicio de Sesión y Recuperación de Contraseña se han simplificado al máximo para evitar la fatiga visual. En la versión móvil, los campos de entrada de datos son los protagonistas absolutos, utilizando etiquetas claras y botones de gran escala. El diseño inclusivo se evidencia en el espaciado entre elementos, optimizado para evitar errores de pulsación y garantizar un acceso rápido incluso para operarios en entornos de alta movilidad.

<div align="center">
  <img src="./../assets/chapter-4/o Registro para Mobile.png" alt="Estilos" width="200"/>
</div>

**Wireframe 3**

El wireframe de Compradores Mobile adapta la experiencia web a un formato de scroll vertical infinito, optimizando el espacio mediante el apilamiento de módulos para una gestión eficiente a una sola mano.

<div align="center">
  <img src="./../assets/chapter-4/Compradores Mobile.png" alt="Estilos" width="200"/>
</div>

**Wireframe 4**

Este wireframe adapta el flujo de compra a una secuencia vertical que guía al usuario de manera lineal desde la configuración hasta la liquidación del pedido. La arquitectura de información se organiza en tres secciones clave: un bloque superior con el resumen detallado de la solicitud de combustible, un carrusel central para la selección de la información de proveedores, y un módulo final dedicado al método de pago.

<div align="center">
  <img src="./../assets/chapter-4/Compradores Mobile pt2 _ Solicitud de Combustible.png" alt="Estilos" width="200"/>
</div>

**Wireframe 5**

Este wireframe presenta el perfil detallado del socio logístico seleccionado, diseñado para fortalecer la transparencia en la cadena de suministro. La arquitectura de información sitúa en la parte superior los datos institucionales y de contacto del proveedor, seguidos de un componente visual de gran formato que representa la ubicación geográfica de sus sedes o estaciones de servicio.

<div align="center">
  <img src="./../assets/chapter-4/Compradores Mobile pt3 _ Información del Proveedor.png" alt="Estilos" width="200"/>
</div>

**Wireframe 6**

El wireframe 6 condensa las herramientas de gestión en una interfaz de alto rendimiento diseñada para la operatividad en campo. La arquitectura de información se organiza verticalmente mediante tres bloques modulares: un Resumen Operativo en la parte superior con tarjetas de métricas clave (ventas, pedidos y flota), seguido de una sección de Pedidos Recientes presentada en filas simplificadas para una validación rápida, y finalmente un carrusel horizontal para el Directorio de Clientes.

<div align="center">
  <img src="./../assets/chapter-4/Proveedores Mobile.png" alt="Estilos" width="200"/>
</div>

**Wireframe 7**

Este wireframe adapta el proceso de vinculación de recursos a una estructura de stacking vertical, permitiendo que el proveedor coordine el transporte de manera secuencial y ordenada.

<div align="center">
  <img src="./../assets/chapter-4/Proveedores Mobile pt2.png" alt="Estilos" width="200"/>
</div>

**Wireframe 8**

Este último wireframe móvil consolida las funciones administrativas de cierre y auditoría en una interfaz simplificada y de fácil navegación. La arquitectura de información mantiene las métricas de resumen en la parte superior para dar contexto antes de proceder a la gestión documental, donde se sitúa un área central de previsualización para los registros de operaciones mensuales.

<div align="center">
  <img src="./../assets/chapter-4/Proveedores Mobile pt3.png" alt="Estilos" width="200"/>
</div>

### 4.4.2 Web Applications Wireflow Diagrams

El diagrama de Wireflow presentado a continuación ilustra la navegación lógica y la interacción entre las diversas interfaces de la plataforma FullTank, detallando el recorrido que realizan tanto proveedores como compradores desde el primer contacto hasta la culminación de sus objetivos operativos. 
El flujo inicia en la Landing Page, la cual actúa como el nodo central de información y conversión. Tras el proceso de Inicio de Sesión/Registro se divide en dos ramas: 

* Flujo de Proveedores: Optimizado para la gestión masiva de datos, este recorrido guía al usuario desde una visión estratégica (Resumen Operativo) hacia acciones tácticas secuenciales, que incluyen la validación de pedidos, la consulta del directorio de clientes, la asignación logística de transporte y la generación de reportes administrativos.

* Flujo de Compradores: Diseñado bajo principios de eficiencia y transparencia, este camino permite al solicitante monitorear su consumo mensual, registrar nuevos pedidos mediante la carga de comprobantes de pago, realizar el seguimiento de su suministro en tiempo real y consultar su historial transaccional.

<div align="center">
  <img src="./../assets/chapter-4/Diagram.png" alt="Estilos" width="1000"/>
</div>

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
