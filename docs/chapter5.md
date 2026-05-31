# Capitulo V: Product Implementation, Validation & Deployment.
## 5.1. Software Configuration Management.
### 5.1.1. Software Development Environment Configuration.

### Project Management

- **WhatsApp**: Aplicación de mensajería instantánea que fue utilizada para coordinar tareas del equipo, interca,biar ideas y brindar soporte continuo durante el desarrollo del proyecto.
- **Google Meet**: Herramienta de videoconferencias de Google empleada para mantener una comunicación verbal y directa, permitiendo la planificación colaborativa de actividades y la toma de decisiones en tiempo real.
- **Microsoft 365**: Servicio en la nube que integra herramientas clásicas como Word y Excel, ofreciendo acceso desde cualquier lugar y permitiendo la colaboración en tiempo real. Permitió la supervisión continua de los avances de los miembros.

### Requirements Management

- **UXPressia**: Herramienta utilizada para la elaboración de User Personas, User Journey Maps e Impact Maps, lo que permite comprender mejor las necesidades de los usuarios y definir funcionalidades centradas en ellos.
- **Zoom**: Aplicación de Google empleada para la toma de entrevistas a potenciales usuarios, facilitando la recopilación de información valiosa para la definición y validación de requisitos.

### Product UX/UI Design

- **Figma**: Plataforma colaborativa utilizada para el diseño de wireframes, wireflows, mockups y prototipos interactivos, garantizando una visión clara y alineada de la interfaz del producto.

### Software Development

- **Visual Studio Code**: Editor de código utilizado para la implementación de la Landing Page, gracias a sus extensiones y soporte para diversas tecnologías web.
- **Google Chrome**: Navegador utilizado para la ejecución de pruebas de visualización y funcionalidad de la landing page y el frontend, asegurando su correcto comportamiento en entornos reales.

### Software Deployment

- **Github Pages**: Servicio de hosting utilizado para el despliegue de la landing page del proyecto.

### Software Documentation

- **Structurizr**: Plataforma empleada para la creación de diagramas C4, permitiendo representar visualmente la arquitectura del software en distintos niveles de abstracción.
- **GitHub**: Plataforma utilizada para la gestión de repositorios de código y documentación del proyecto, incluyendo la landing page, el frontend, el backend y los documentos técnicos, facilitando el trabajo colaborativo y el control de versiones.
- **Vertabelo**: Herramienta especializada en el modelado de bases de datos, utilizada para diseñar diagramas entidad-relación (ERD), permitiendo estructurar de manera clara y eficiente la arquitectura de datos del sistema.
- **Trello**: Herramienta de gestión ágil utilizada para la organización del Product Backlog y Sprint Backlog, permitiendo priorizar tareas, hacer seguimiento del progreso y coordinar el trabajo del equipo de manera colaborativa.


### 5.1.2. Source Code Management.

El proyecto utiliza GitHub como repositorio para administrar y estructurar los avances. Implementamos el flujo de trabajo **Gitflow**, siguiendo la metodología propuesta por Vincent Driessen, para mantener versiones estables y trabajo colaborativo ordenado.

**Main branch:** Rama principal donde se almacena el código de producción estable.

**Develop branch:** Rama de integración donde se fusionan las nuevas funcionalidades desarrolladas.

**Chapter branches:** Ramas creadas a partir de `develop` para seccionar los avances del proyecto por capítulo. Cada chapter se trabaja de forma aislada para evitar conflictos.

**Conventional Commits:** Estándar aplicado en los mensajes de commit para mantener un historial de cambios claro, comprensible y trazable, mejorando además la automatización de flujos de despliegue.

**Feature branches:** Creadas desde `develop` con la convención 
`feature/[bounded-context]-[descripción]`.  
Ejemplo: `feature/ordering-create-request`, `feature/fulfillment-fleet`

**Release branches:** Creadas desde `develop` cuando el Sprint 
está listo para producción, con la convención `release/vX.Y.Z` 
siguiendo Semantic Versioning (MAJOR.MINOR.PATCH).  
Ejemplo: `release/v1.0.0`, `release/v1.1.0`

**Hotfix branches:** Creadas desde `main` para correcciones 
urgentes en producción, con la convención `hotfix/[descripción]`.  
Ejemplo: `hotfix/fix-login-redirect`

**Semantic Versioning:** Los releases del proyecto siguen el 
estándar vMAJOR.MINOR.PATCH donde:
- MAJOR: cambio incompatible con versión anterior
- MINOR: nueva funcionalidad compatible
- PATCH: corrección de bugs

### 5.1.3. Source Code Style Guide & Conventions.

**HTML:**

Seguimos las convenciones descritas en la guía oficial HTML Style Guide and Coding Conventions para fomentar una estructura limpia, semántica y predecible:

- Usar nombres de elementos en minúsculas.
- Cerrar todos los elementos HTML, incluso los que son opcionales.
- Usar nombres de atributos en minúsculas.
- Incluir siempre los atributos requeridos en elementos clave, especialmente en imágenes (alt) y formularios (name, id, etc.).
- Evitar líneas de código largas para mejorar la legibilidad.
- Utilizar sintaxis simplificada y estándar para hojas de estilo (link) y scripts externos (script).

**CSS:**

Aplicamos las siguientes convenciones para lograr un estilo consistente, ordenado y fácil de mantener:

- Usar minúsculas y guiones para los nombres de clases y selectores.
- Escribir un espacio después de los dos puntos y cerrar cada declaración con punto y coma.
- Agrupar reglas CSS relacionadas y separarlas con una línea en blanco para mejorar la claridad visual.
- Utilizar nombres de clases descriptivos, que reflejen la función o apariencia del elemento.
- Organizar el CSS por bloques lógicos o módulos.

**JavaScript:**

Definimos las siguientes convenciones para asegurar un código robusto, eficiente y comprensible:

- Declarar las variables al inicio del ámbito correspondiente, evitando la redeclaración innecesaria.
- Preferir el uso de const y let en lugar de var para controlar mejor el ámbito y la mutabilidad de las variables.
- Incluir comentarios descriptivos para explicar la funcionalidad de componentes, servicios, validaciones y lógica compleja.
- Mantener las funciones pequeñas y con una única responsabilidad.
- Aplicar principios de programación funcional y reactiva, así como patrones de diseño adecuados.

**Vue (Vue Style Guide):**

- Nombres de componentes en PascalCase: `FuelOrderCard.vue`
- Un componente por archivo
- Props definidas con tipo y valor por defecto usando defineProps()
- Directivas abreviadas: `:` para v-bind, `@` para v-on, `#` para v-slot
- Emits declarados explícitamente con defineEmits()
- Composables con prefijo `use`: `useOrderStore`, `useAuthStore`
- Bounded contexts organizados como módulos independientes

**C# / ASP.NET Core (C# Coding Conventions + Microsoft ASP.NET Core):**

- PascalCase para clases, métodos y propiedades públicas
- camelCase para variables locales y parámetros
- Interfaces con prefijo "I": `IOrderRepository`, `IPaymentService`
- Async/await para todas las operaciones de I/O
- Endpoints REST en plural y minúsculas: `GET /api/orders`, 
  `POST /api/payments`
- DTOs separados de entidades de dominio
- Inyección de dependencias mediante constructor

### 5.1.4. Software Deployment Configuration.

#### Entorno de Desarrollo

Tecnologías utilizadas:
- HTML5
- CSS3
- Javascript

#### Estrategia de Deployment

- Github Pages
- Repositorio principal en GitHub

Flujo Gitflow:

- main: rama principal de producción
- develop: rama de integración principal
- chapter-n*: desarrollo de los chapters sobre develop
- Pull Requests se realizan desde chapter-n hacia develop

## 5.2. Landing Page, Services & Applications Implementation.

### 5.2.1. Sprint 1

#### 5.2.1.1. Sprint Planning 1.

<table border>
    <tr align="center">
        <td><strong>Sprint #</strong></td>
        <td><strong>Sprint 1</strong></td>
    </tr>
    <tr>
        <td colspan="2" align="center"><strong>Sprint Planning Background</strong></td>
    </tr>
    <tr align="center">
        <td>Date</td>
        <td>09/04/2026</td>
    </tr>
    <tr align="center">
        <td>Time</td>
        <td>15:00 PM</td>
    </tr>
    <tr align="center">
        <td>Location</td>
        <td>Meet</td>
    </tr>
    <tr align="center">
        <td>Prepared by</td>
        <td>Milenko Cayanchi</td>
    </tr>
    <tr align="center">
        <td>Attendess (to planning meeting)</td>
        <td>
          Milenko Rubén Cayanchi Avila - u202312566<br>
          Jose Gustavo Asto Jacome - u20241c630<br>
          Alberto Alejandro Ponce Perales - u202320684<br>
          Diego Fernando Herrera Enriquez - u202319027<br>
          Brayan Alexis Corvacho Damian - u20231a257
        </td>
    </tr>
    <tr align="center">
        <td>Sprint 0 Review Summary</td>
        <td>No hubo sprint previo</td>
    </tr>
    <tr align="center">
        <td>Sprint 0 Retrospective Summary</td>
        <td>No hubo sprint previo</td>
    </tr>
    <tr>
        <td colspan="2" align="center"><strong>Sprint Goal & User Stories</strong></td>
    </tr>
    <tr>
        <td align="center">Sprint 1 Goal</td>
        <td>Desarrollar una landing page funcional y visualmente clara que comunique efectivamente la propuesta de valor de FullTank a nuestros dos segmentos clave de usuarios: proveedores de combustible y solicitantes de combustible. La página debe incluir secciones estratégicas como:<br>
          <ul>
            <li><strong>Our focus is on:</strong> communicating FullTank's value proposition to fuel requesters and suppliers through a deployed landing page.</li>
            <li><strong>We believe:</strong> it delivers clarity on the platform's benefits and increases sign-up intent for both customer segments.</li>
            <li><strong>This will be confirmed when:</strong> both segments can navigate the landing page, understand the service, and access contact and demo request options without assistance.</li>
          </ul>
    </tr>
    <tr align="center">
        <td>Sprint 1 Velocity</td>
        <td>12</td>
    </tr>
    <tr align="center">
        <td>Sum of Story Point</td>
        <td>17</td>
    </tr>
</table>

#### 5.2.1.2. Aspect Leaders and Collaborators.

<table border="1" cellspacing="0" cellpadding="6">
  <thead>
    <tr>
      <th>Team Member</th>
      <th>GitHub Username</th>
      <th>Landing Page</th>
      <th>Documentation</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Milenko Rubén Cayanchi Avila</td>
      <td>MaxghZZ</td>
      <td>L</td>
      <td>L</td>
    </tr>
    <tr>
      <td>Jose Gustavo Asto Jacome</td>
      <td>DhudsQ</td>
      <td>C</td>
      <td>C</td>
    </tr>
    <tr>
      <td>Diego Fernando Herrera Enriquez</td>
      <td>TheBlackunityrogue</td>
      <td>C</td>
      <td>C</td>
    </tr>
    <tr>
      <td>Alberto Alejandro Ponce Perales</td>
      <td>aponceperales</td>
      <td>C</td>
      <td>C</td>
    </tr>
    <tr>
      <td>Brayan Alexis Corvacho Damian</td>
      <td>BralexCD</td>
      <td>C</td>
      <td>C</td>
    </tr>
  </tbody>
</table>

#### 5.2.1.3. Sprint Backlog 1.

<table border>
    <tr align="center">
        <td colspan="2"><strong>Sprint #</strong></td>
        <td colspan="6"><strong>Sprint 1</strong></td>
    </tr>
    <tr align="center">
        <td colspan="2"><strong>User Story</strong></td>
        <td colspan="6"><strong>Work-Item / Task</strong></td>
    </tr>
    <tr align="center">
        <td><strong>Id</strong></td>
        <td><strong>Title</strong></td>
        <td><strong>Id</strong></td>
        <td><strong>Title</strong></td>
        <td><strong>Description</strong></td>
        <td><strong>Estimation (Hours)</strong></td>
        <td><strong>Assigned to</strong></td>
        <td><strong>Status (To do / In process / To review / Done)</strong></td>
    </tr>
    <tr align="center">
        <td>US-01</td>
        <td>Ver sección Home</td>
        <td>W-01</td>
        <td>Sección Home</td>
        <td>Como visitante (proveedor), quiero ver una sección de inicio que resuma el valor de FullTank para comprender rápidamente el objetivo del sistema</td>
        <td>5 horas</td>
        <td>Ruben Milenko</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-02</td>
        <td>Ver sección About Us</td>
        <td>W-02</td>
        <td>Sección About Us</td>
        <td>Como visitante de ambos segmentos, quiero conocer quiénes están detrás de FullTank para confiar en el sistema</td>
        <td>4 horas</td>
        <td>Jose Asto</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-03</td>
        <td>Ver sección How it Works?</td>
        <td>W-03</td>
        <td>Sección How it works?</td>
        <td>Como visitante de ambos segmentos, quiero entender cómo funciona FullTank paso a paso para evaluar si se ajusta a mis necesidades</td>
        <td>5 horas</td>
        <td>Enrique Mantilla</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-36</td>
        <td>Ver sección Benefits</td>
        <td>W-04</td>
        <td>Sección Beneficios</td>
        <td>Como visitante de ambos segmentos, quiero conocer las principales ventajas con las que puedo contar para evaluar la implementación de la plataforma</td>
        <td>4 horas</td>
        <td>Enrique Mantilla</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-37</td>
        <td>Ver sección Testimonios</td>
        <td>W-05</td>
        <td>Sección Testimonios</td>
        <td>Como visitante de ambos segmentos, quiero conocer los testimonios de los usuarios de FullTank para tener confianza en la plataforma</td>
        <td>6 horas</td>
        <td>Brayan Corvacho</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-04</td>
        <td>Enviar mensaje de contacto</td>
        <td>W-06</td>
        <td>Contacto</td>
        <td>Como visitante de ambos segmentos, quiero enviar un mensaje desde Contact Us para solicitar más información</td>
        <td>5 horas</td>
        <td>Jose Asto</td>
        <td>In Process</td>
    </tr>
    <tr align="center">
        <td>US-38</td>
        <td>Ver sección Planes y Precios</td>
        <td>W-07</td>
        <td>Sección Planes y Precios</td>
        <td>Como visitante (ambos segmentos), quiero saber que planes se adecuan a mis necesidades</td>
        <td>6 horas</td>
        <td>Ruben Milenko</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-39</td>
        <td>Cambiar idioma</td>
        <td>W-08</td>
        <td>Idioma</td>
        <td>Como visitante de ambos segmentos, quiero poder cambiar entre inglés y español</td>
        <td>8 horas</td>
        <td>Enrique Mantilla</td>
        <td>In Process</td>
    </tr>
</table>

#### 5.2.1.4. Development Evidence for Sprint Review.

Durante el Sprint 1, nuestro equipo culminó la implementación de la Landing Page de FullTank, cumpliendo con las User Stories priorizadas. Se trabajó en la maquetación de las secciones principales, implementación de estilos CSS, diseño responsive para diferentes dispositivos y subida de los cambios al repositorio grupal. Los commits fueron realizados en la rama main, cada uno agregando una sección de la Landing Page

<table border>
  <thead>
    <tr>
      <th>Repositorio</th>
      <th>Rama</th>
      <th>ID de Commit</th>
      <th>Mensaje de Commit</th>
      <th>Descripción del Commit</th>
      <th>Fecha de Commit</th>
    </tr>
  </thead>
<tbody>
  <tr>
    <td>TechnoSAC/FullTank_LandingPage</td>
    <td>main</td>
    <td>fe56813</td>
    <td>feat: initialize landing page structure with HTML, CSS, JavaScript</td>
    <td>Autor: Ruben Milenko - Inicialización del proyecto base del landing page</td>
    <td>23/04/2026</td>
  </tr>
  <tr>
    <td>TechnoSAC/FullTank_LandingPage</td>
    <td>main</td>
    <td>12a321b</td>
    <td>feat: create landing page structure with navigation and hero</td>
    <td>Autor: Ruben Milenko - Creación de estructura principal y navegación</td>
    <td>23/04/2026</td>
  </tr>
  <tr>
    <td>TechnoSAC/FullTank_LandingPage</td>
    <td>main</td>
    <td>81e8d95</td>
    <td>feat: add FAQ section, final CTA, and footer</td>
    <td>Autor: Ruben Milenko - Implementación de secciones finales del landing</td>
    <td>23/04/2026</td>
  </tr>
  <tr>
    <td>TechnoSAC/FullTank_LandingPage</td>
    <td>main</td>
    <td>a348d6d</td>
    <td>feat: initialize global CSS styles with design tokens</td>
    <td>Autor: Ruben Milenko - Definición de estilos globales</td>
    <td>23/04/2026</td>
  </tr>
  <tr>
    <td>TechnoSAC/FullTank_LandingPage</td>
    <td>main</td>
    <td>870e2fd</td>
    <td>feat: add styles for metrics, FAQ, navigation</td>
    <td>Autor: Ruben Milenko - Estilos para componentes clave</td>
    <td>23/04/2026</td>
  </tr>
  <tr>
    <td>TechnoSAC/FullTank_LandingPage</td>
    <td>main</td>
    <td>f8989c6</td>
    <td>feat: add styling for sections like pricing and features</td>
    <td>Autor: Ruben Milenko - Mejora visual de secciones principales</td>
    <td>23/04/2026</td>
  </tr>
  <tr>
    <td>TechnoSAC/FullTank_LandingPage</td>
    <td>main</td>
    <td>aef477a</td>
    <td>feat: add responsive team section styles</td>
    <td>Autor: Ruben Milenko - Implementación responsive del equipo</td>
    <td>23/04/2026</td>
  </tr>
  <tr>
    <td>TechnoSAC/FullTank_LandingPage</td>
    <td>main</td>
    <td>c7782c5</td>
    <td>feat: implement navbar scroll effects and mobile navigation</td>
    <td>Autor: Ruben Milenko - Interacciones dinámicas del navbar</td>
    <td>23/04/2026</td>
  </tr>
  <tr>
    <td>TechnoSAC/FullTank_LandingPage</td>
    <td>main</td>
    <td>2f6d95a</td>
    <td>feat: implement interactive features like pricing toggle</td>
    <td>Autor: Ruben Milenko - Funcionalidades interactivas del landing</td>
    <td>23/04/2026</td>
  </tr>
  <tr>
    <td>TechnoSAC/FullTank_LandingPage</td>
    <td>main</td>
    <td>9b1914e</td>
    <td>fix: added photos and names in About Us</td>
    <td>Autor: Enrique Mantilla - Actualización de sección About Us</td>
    <td>25/04/2026</td>
  </tr>
  <tr>
    <td>TechnoSAC/FullTank_LandingPage</td>
    <td>main</td>
    <td>665a936</td>
    <td>fix: improve english translate</td>
    <td>Autor: Enrique Mantilla - Mejora de traducciones</td>
    <td>25/04/2026</td>
  </tr>
  <tr>
    <td>TechnoSAC/FullTank_LandingPage</td>
    <td>main</td>
    <td>172f37d</td>
    <td>fix: update team description with creative focus</td>
    <td>Autor: Enrique Mantilla - Ajuste de contenido del equipo</td>
    <td>26/04/2026</td>
  </tr>
  <tr>
    <td>TechnoSAC/FullTank_LandingPage</td>
    <td>main</td>
    <td>ddba9ff</td>
    <td>UI: Improves the style of several sections</td>
    <td>Autor: Enrique Mantilla - Mejora de estilos visuales</td>
    <td>26/04/2026</td>
  </tr>
  <tr>
    <td>TechnoSAC/FullTank_LandingPage</td>
    <td>main</td>
    <td>a4c9c91</td>
    <td>feat: add video redirect to team action button</td>
    <td>Autor: Enrique Mantilla - Nueva funcionalidad en botón</td>
    <td>26/04/2026</td>
  </tr>
  <tr>
    <td>TechnoSAC/FullTank_LandingPage</td>
    <td>main</td>
    <td>ff0b02d</td>
    <td>fix: correction of spelling errors</td>
    <td>Autor: Enrique Mantilla - Corrección de textos</td>
    <td>26/04/2026</td>
  </tr>
  <tr>
    <td>TechnoSAC/FullTank_LandingPage</td>
    <td>main</td>
    <td>eb51c66</td>
    <td>fix: correct file paths for assets and update team information</td>
    <td>Autor: Jose Asto - Corrección de rutas y contenido</td>
    <td>26/04/2026</td>
  </tr>
  <tr>
    <td>TechnoSAC/FullTank_LandingPage</td>
    <td>main</td>
    <td>0a796b0</td>
    <td>fix(main.js): minor translation problems fixed</td>
    <td>Autor: Jose Asto - Ajustes menores en traducciones</td>
    <td>26/04/2026</td>
  </tr>
</tbody>
</table>

#### 5.2.1.5. Execution Evidence for Sprint Review.

En el sprint 1 se diseñó el primer modelo de la landing page. Esta cuenta con diferentes secciones para acceso de los usuarios. Algunas evidencias son:
- **Home:** Presenta de manera rápida el propósito y valor de FullTank para captar la atención del visitante.
![Home](../assets/chapter-5/home.png)

- **About Us:** Explica quiénes somos y nuestra misión para generar confianza.
![About Us](../assets/chapter-5/about-us.png)

- **Benefits:** Explica los beneficios de implementar FullTank en el área logística de la empresa.
![How it works?](../assets/chapter-5/benefits.png)

- **How it works?:** Describe de forma sencilla y visual el funcionamiento de FullTank paso a paso.
![How it works?](../assets/chapter-5/how-it-works.png)

- **Testimonials:** Muestra algunas de las empresas o usuarios que confían en FullTank como referencia de credibilidad.
![Our Clients](../assets/chapter-5/testimonials.png)

- **Pricing:** Propone planes y precios que puedan acomodarse a las necesidades del usuario.
![Join](../assets/chapter-5/pricing.png)

- **Contact Us:** Ofrece un formulario y datos de contacto directo para resolver dudas o solicitar soporte.
![Contact Us](../assets/chapter-5/contact.png)

#### 5.2.1.6. Services Documentation Evidence for Sprint Review.

Durante el Sprint 1, el equipo se enfocó en el desarrollo del Landing Page de FullTank, por lo cual no se implementaron ni documentaron endpoints relacionados a Web Services. Los trabajos de desarrollo backend, integración de API y documentación con OpenAPI están planificados para Sprints posteriores.

#### 5.2.1.7. Software Deployment Evidence for Sprint Review.

<p>
    <strong>Resumen:</strong><br>
    El despliegue inicial de la Landing Page de FullTank fue realizado exitosamente utilizando Vercel.
</p>

<h4>Detalles del Despliegue:</h4>

<ul>
  <li><strong>URL de la Landing Page:</strong> <a href="https://technosac.github.io/FullTank_LandingPage/" target="_blank">https://technosac.github.io/FullTank_LandingPage/</a></li>
  <li><strong>Repositorio:</strong> <a href="https://github.com/TechnoSAC/FullTank_LandingPage/settings/pages" target="_blank">https://github.com/TechnoSAC/FullTank_LandingPage/settings/pages</a></li>
</ul>

<h4>Evidencia:</h4>

![Deployment Visual Evidence of Analytics](../assets/chapter-5/deploy-analytics.png)

#### 5.2.1.8. Team Collaboration Insights during Sprint. 

<p>
    <strong>Resumen:</strong><br>
    El equipo colaboró mediante GitHub y WhatsApp durante el Sprint. Las actividades principales se centraron en el desarrollo y despliegue de la Landing Page.
</p>

<h4>Evidencia de Colaboración:</h4>
<ul>
  <li>Captura de pantalla de commits en GitHub mostrando contribuciones del equipo.</li>
  
  ![Collaboration of the team](../assets/chapter-5/contributors.png)
</ul>

<h4>Principales Herramientas de Comunicación:</h4>
<ul>
  <li>GitHub (control de versiones y manejo de issues)</li>
  <li>WhatsApp (comunicación diaria y aclaraciones rápidas)</li>
  <li>Google Meet (reuniones de planificación de sprint)</li>
</ul>

### 5.2.2. Sprint 2

#### 5.2.2.1. Sprint Planning 2.

<table border>
    <tr align="center">
        <td><strong>Sprint #</strong></td>
        <td><strong>Sprint 2</strong></td>
    </tr>
    <tr>
        <td colspan="2" align="center"><strong>Sprint Planning Background</strong></td>
    </tr>
    <tr align="center">
        <td>Date</td>
        <td>27/04/2026</td>
    </tr>
    <tr align="center">
        <td>Time</td>
        <td>15:00 PM</td>
    </tr>
    <tr align="center">
        <td>Location</td>
        <td>Meet / Discord</td>
    </tr>
    <tr align="center">
        <td>Prepared by</td>
        <td>Milenko Cayanchi</td>
    </tr>
    <tr align="center">
        <td>Attendees (to planning meeting)</td>
        <td>
          Milenko Rubén Cayanchi Avila<br>
          Jose Gustavo Asto Jacome<br>
          Enrique Manuel Mantilla Maldonado<br>
          Brayan Alexis Corvacho Damian
        </td>
    </tr>
    <tr align="center">
        <td>Sprint 1 Review Summary</td>
        <td>Se logró desplegar con éxito la Landing Page en GitHub Pages. El feedback general fue positivo y los estilos fueron consistentes.</td>
    </tr>
    <tr align="center">
        <td>Sprint 1 Retrospective Summary</td>
        <td>El equipo trabajó de forma coordinada, pero identificamos que necesitamos definir la arquitectura inicial del proyecto Frontend en Vue antes de avanzar a múltiples vistas.</td>
    </tr>
    <tr>
        <td colspan="2" align="center"><strong>Sprint Goal & User Stories</strong></td>
    </tr>
    <tr>
        <td align="center">Sprint 2 Goal</td>
        <td>
          Our focus is on delivering a functional and navigable 
          Frontend Web Application covering FullTank's core 
          operational flows.
          We believe it delivers a first operational experience 
          to fuel providers, enabling simulation of inventory 
          management, order processing and fleet dispatch.
          This will be confirmed when users can navigate all 
          main modules (dashboard, inventory, ordering, 
          fulfillment, reporting) in the deployed Firebase 
          app without critical navigation failures.
        </td>
    </tr>
    <tr align="center">
        <td>Sprint 2 Velocity</td>
        <td>15</td>
    </tr>
    <tr align="center">
        <td>Sum of Story Point</td>
        <td>21</td>
    </tr>
</table>

#### 5.2.2.2. Aspect Leaders and Collaborators.

<table border="1" cellspacing="0" cellpadding="6">
  <thead>
    <tr>
      <th>Team Member</th>
      <th>GitHub Username</th>
      <th>Frontend Core / Structure</th>
      <th>Frontend Modules / UI</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Milenko Rubén Cayanchi Avila</td>
      <td>MaxghZZ</td>
      <td>L</td>
      <td>L</td>
    </tr>
    <tr>
      <td>Jose Gustavo Asto Jacome</td>
      <td>DhudsQ</td>
      <td>C</td>
      <td>L</td>
    </tr>
    <tr>
      <td>Enrique Manuel Mantilla Maldonado</td>
      <td>enrique-mantilla</td>
      <td>C</td>
      <td>C</td>
    </tr>
    <tr>
      <td>Brayan Alexis Corvacho Damian</td>
      <td>BralexCD</td>
      <td>C</td>
      <td>C</td>
    </tr>
    </tbody>
</table>


#### 5.2.2.3. Sprint Backlog 2.

<table border>
    <tr align="center">
        <td colspan="2"><strong>Sprint #</strong></td>
        <td colspan="6"><strong>Sprint 2</strong></td>
    </tr>
    <tr align="center">
        <td colspan="2"><strong>User Story</strong></td>
        <td colspan="6"><strong>Work-Item / Task</strong></td>
    </tr>
    <tr align="center">
        <td><strong>Id</strong></td>
        <td><strong>Title</strong></td>
        <td><strong>Id</strong></td>
        <td><strong>Title</strong></td>
        <td><strong>Description</strong></td>
        <td><strong>Estimation (Hours)</strong></td>
        <td><strong>Assigned to</strong></td>
        <td><strong>Status</strong></td>
    </tr>
    <tr align="center">
        <td>US-18</td>
        <td>Ver Dashboard del proveedor</td>
        <td>W-14</td>
        <td>Dashboard Principal</td>
        <td>Implementación del dashboard con KPIs de combustible vendido, tendencias y navegación operativa.</td>
        <td>6 horas</td>
        <td>Jose Asto</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-19</td>
        <td>Ver resumen de pedidos (Proveedor)</td>
        <td>W-15</td>
        <td>KPIs Operativos</td>
        <td>Visualización de métricas y resumen de pedidos activos, despachados y finalizados.</td>
        <td>4 horas</td>
        <td>Jose Asto</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-20</td>
        <td>Gestionar inventario</td>
        <td>W-16</td>
        <td>Módulo Inventory</td>
        <td>CRUD completo de productos y catálogo de combustibles usando PrimeVue y conexión con json-server.</td>
        <td>6 horas</td>
        <td>Ruben Milenko</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-10</td>
        <td>Ver pedidos pendientes</td>
        <td>W-17</td>
        <td>Lista de Solicitudes</td>
        <td>Visualización de solicitudes pendientes y estados de órdenes desde el módulo Ordering.</td>
        <td>5 horas</td>
        <td>Enrique Mantilla</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-11</td>
        <td>Aprobar pedido</td>
        <td>W-18</td>
        <td>Aprobación de Pedidos</td>
        <td>Implementación de acciones para aprobar pedidos y actualizar estados operativos.</td>
        <td>4 horas</td>
        <td>Enrique Mantilla</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-42</td>
        <td>Rechazar pedido</td>
        <td>W-19</td>
        <td>Rechazo de Pedidos</td>
        <td>Implementación de flujo para rechazo de pedidos y actualización de estado.</td>
        <td>3 horas</td>
        <td>Enrique Mantilla</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-12</td>
        <td>Marcar pedido como despachado</td>
        <td>W-20</td>
        <td>Despacho de Pedidos</td>
        <td>Actualización de estados de órdenes a “Despachado” desde el detalle operativo.</td>
        <td>3 horas</td>
        <td>Enrique Mantilla</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-13</td>
        <td>Cerrar pedido</td>
        <td>W-21</td>
        <td>Cierre Operativo</td>
        <td>Implementación del cierre de pedidos luego de la confirmación de entrega.</td>
        <td>3 horas</td>
        <td>Enrique Mantilla</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-44</td>
        <td>Gestionar vehículos de flota</td>
        <td>W-22</td>
        <td>Módulo Vehículos</td>
        <td>CRUD completo para la gestión de vehículos disponibles para despacho.</td>
        <td>5 horas</td>
        <td>Brayan Corvacho</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-45</td>
        <td>Gestionar conductores</td>
        <td>W-23</td>
        <td>Módulo Conductores</td>
        <td>CRUD completo de conductores y control de disponibilidad operativa.</td>
        <td>5 horas</td>
        <td>Brayan Corvacho</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-34</td>
        <td>Ver gráfico de ventas (Proveedor)</td>
        <td>W-24</td>
        <td>Analytics de Ventas</td>
        <td>Implementación de gráficos estadísticos usando Chart.js para visualizar ventas mensuales.</td>
        <td>4 horas</td>
        <td>Jose Asto</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-48</td>
        <td>Ver distribución de ventas por sector</td>
        <td>W-25</td>
        <td>Distribución por Sector</td>
        <td>Visualización analítica de ventas segmentadas por sector industrial.</td>
        <td>4 horas</td>
        <td>Jose Asto</td>
        <td>Done</td>
    </tr>
    <tr align="center">
        <td>US-31</td>
        <td>Ver listado de empresas</td>
        <td>W-26</td>
        <td>Portafolio de Clientes</td>
        <td>Listado interactivo de empresas solicitantes y visualización de información comercial.</td>
        <td>4 horas</td>
        <td>Jose Asto</td>
        <td>Done</td>
    </tr>
</table>

#### 5.2.2.4. Development Evidence for Sprint Review.

Durante el Sprint 2, el equipo se enfocó en el repositorio `frontend`. El desarrollo se construyó sobre **Vue 3.5**, **Vite 8**, y el ecosistema **PrimeVue 4.5** con PrimeFlex. Para el manejo de estados usamos **Pinia**, consumo de APIs vía **Axios** conectado a un **json-server** de prueba y gráficas con **Chart.js**. El proyecto además incluyó traducciones (`locales/es.json`, `en.json`) usando vue-i18n.

<table border>
  <thead>
    <tr>
      <th>Repositorio</th>
      <th>Rama</th>
      <th>ID de Commit</th>
      <th>Mensaje de Commit</th>
    </tr>
  </thead>
<tbody>
  <tr>
    <td>TechnoSAC/frontend</td>
    <td>main</td>
    <td>ea05c79</td>
    <td>feature(inventory): render product form with PrimeVue components.</td>
  </tr>
  <tr>
    <td>TechnoSAC/frontend</td>
    <td>main</td>
    <td>4be7a68</td>
    <td>feat(ordering): added vue components and solved shared problems with ordering</td>
  </tr>
  <tr>
    <td>TechnoSAC/frontend</td>
    <td>main</td>
    <td>8f26e18</td>
    <td>feat(fulfillment): added dispatch view</td>
  </tr>
  <tr>
    <td>TechnoSAC/frontend</td>
    <td>main</td>
    <td>d4e438b</td>
    <td>feat(dashboard): added dashboard page</td>
  </tr>
  <tr>
    <td>TechnoSAC/frontend</td>
    <td>main</td>
    <td>ff997c7</td>
    <td>feat(reporting): added graphics and db.json information for reporting</td>
  </tr>
  <tr>
    <td>TechnoSAC/frontend</td>
    <td>main</td>
    <td>0d34f20</td>
    <td>fix(dashboard): fixed bug in showing the bar graph</td>
  </tr>
  <tr>
    <td>TechnoSAC/frontend</td>
    <td>main</td>
    <td>1c48057</td>
    <td>fix(reporting): changed titles and added db.json information</td>
  </tr>
  <tr>
    <td>TechnoSAC/frontend</td>
    <td>main</td>
    <td>658cf6a</td>
    <td>fix(shared): fixed bug in shared, double selection in inventory</td>
  </tr>
</tbody>
</table>

#### 5.2.2.5. Execution Evidence for Sprint Review.

En este sprint se implementaron las siguientes pantallas y módulos clave:

* **Dashboard Principal:** Vista principal con KPIs de combustible, tendencia de ventas usando Chart.js y sidebar de navegación compartida.
![Dashboard View](../assets/chapter-5/dashboard.png)

* **Inventario (Inventory):** Lista de productos/combustibles en tabla PrimeVue con acciones CRUD integradas.
![Inventory View](../assets/chapter-5/inventory.png)

* **Gestión de Órdenes (Ordering):** Visualización de solicitudes y detalle de órdenes donde el usuario puede aprobar, rechazar o cambiar estado a despachado.
![Ordering View](../assets/chapter-5/ordering.png)

* **Despacho y Flota (Vehículos):** Gestión de la flota de vehículos con filtros por disponibilidad y registro CRUD completo.
![Vehicles View](../assets/chapter-5/fulfillment-vehicles.png)

* **Despacho y Flota (Conductores):** Control del registro de conductores autorizados y asignación de estados operativos.
![Drivers View](../assets/chapter-5/fulfillment-drivers.png)

#### 5.2.2.6. Services Documentation Evidence for Sprint Review.

Durante el Sprint 2 se utilizó un Mock API (json-server) desplegado 
en Render (`https://json-server-1-1uka.onrender.com`) para simular 
los endpoints del RESTful API. La implementación real con ASP.NET Core 
y documentación OpenAPI/Swagger está planificada para Sprint 3.

A continuación se detallan los endpoints simulados utilizados:

| Endpoint       | Verbo HTTP | Descripción                              | Parámetros                                              | Response                   |
| -------------- | ---------- | ---------------------------------------- | ------------------------------------------------------- | -------------------------- |
| /inventory     | GET        | Lista todos los productos de combustible | -                                                       | 200 + array de productos   |
| /inventory     | POST       | Registra nuevo producto                  | body: {fuel_type, quantity_liters, price_per_liter}     | 201 + producto creado      |
| /inventory/:id | PUT        | Actualiza producto existente             | id, body: {fuel_type, quantity_liters, price_per_liter} | 200 + producto actualizado |
| /inventory/:id | DELETE     | Elimina producto                         | id                                                      | 200                        |
| /orders        | GET        | Lista todas las solicitudes              | -                                                       | 200 + array de órdenes     |
| /orders/:id    | GET        | Obtiene detalle de una solicitud         | id                                                      | 200 + objeto orden         |
| /orders/:id    | PATCH      | Actualiza estado de orden                | id, body: {status}                                      | 200 + orden actualizada    |
| /transports    | GET        | Lista vehículos de flota                 | -                                                       | 200 + array de vehículos   |
| /transports    | POST       | Registra vehículo                        | body: {plate, vehicle_type, capacity_liters}            | 201 + vehículo creado      |
| /drivers       | GET        | Lista conductores                        | -                                                       | 200 + array de conductores |
| /drivers       | POST       | Registra conductor                       | body: {full_name, dni, license_number}                  | 201 + conductor creado     |
| /reports       | GET        | Lista reportes generados                 | -                                                       | 200 + array de reportes    |

**URL del repositorio Frontend:** https://github.com/TechnoSAC/frontend  


#### 5.2.2.7. Software Deployment Evidence for Sprint Review.

<p>
    <strong>Resumen:</strong><br>
    Se logró el despliegue automático de la aplicación Frontend en la nube utilizando Firebase Hosting. El proyecto está configurado a través del archivo `firebase.json` en el workspace `full-tank-964e2`.
</p>

<h4>Detalles del Despliegue:</h4>
<ul>
  <li><strong>URL del Frontend App:</strong> <a href="https://full-tank-964e2.web.app/" target="_blank">https://full-tank-964e2.web.app/</a></li>
  <li><strong>URL Alternativa:</strong> <a href="https://full-tank-964e2.firebaseapp.com/" target="_blank">https://full-tank-964e2.firebaseapp.com/</a></li>
  <li><strong>Repositorio Frontend:</strong> <a href="https://github.com/TechnoSAC/frontend" target="_blank">https://github.com/TechnoSAC/frontend</a></li>
</ul>

<h4>Evidencia de Despliegue:</h4>

![Frontend Firebase Deployment](../assets/chapter-5/firebase-deploy.png)

#### 5.2.2.8. Team Collaboration Insights during Sprint. 

<p>
    <strong>Resumen:</strong><br>
    La colaboración se estructuró dividiendo los componentes de Vue según los módulos del negocio: <b>Milenko</b> estructuró las bases, layout, router y Pinia config; <b>Jose Asto</b> integró dashboards, dispatch view y resolvió bugs de layout; <b>Enrique Mantilla</b> lideró el módulo reporting; <b>Brayan Corvacho</b> conectó UI con PrimeVue y consumo Axios.
</p>

<h4>Evidencia de Colaboración (GitHub Frontend):</h4>
<ul>
  <li>Captura de los Contribuidores del repositorio Frontend en GitHub.</li>
</ul>

![Frontend Contributors](../assets/chapter-5/frontend-contributors.png)

<br>

**Conclusiones**

Al finalizar el ciclo de desarrollo y validación de la solución FullTank, el equipo ha llegado a las siguientes conclusiones, contrastando los resultados obtenidos con los planteamientos iniciales del proceso Lean UX:

1. Validación de Problem Statements y Supuestos (Assumptions):

Inicialmente, se estableció como Problem Statement que las empresas que gestionan combustible enfrentan ineficiencias operativas debido a procesos manuales, falta de trazabilidad y poca visibilidad en la cadena de suministro. Tras las pruebas de validación, se confirmó que la digitalización del ciclo de pedidos, junto con el monitoreo en tiempo real, reduce significativamente los errores operativos y mejora la eficiencia logística.

Asimismo, se validó el supuesto de que los usuarios están dispuestos a adoptar soluciones digitales siempre que estas simplifiquen sus procesos y centralicen la información. Sin embargo, el supuesto de que los usuarios priorizaban únicamente el registro de pedidos fue refutado; las pruebas evidenciaron que existe una alta demanda por funcionalidades de seguimiento en tiempo real y notificaciones automáticas, lo que llevó a priorizar estas características dentro del sistema.

2. Contrastación de Hipótesis (Hypothesis Statements):

Hipótesis de Valor para Empresas:
Se planteó que "Si proporcionamos un dashboard centralizado, las empresas podrán optimizar la gestión de combustible y reducir errores en los pedidos". Los resultados de las pruebas de usabilidad confirmaron esta hipótesis, destacando que la visualización consolidada de pedidos, consumos y estados de entrega fue una de las funcionalidades más valoradas por los usuarios.

Hipótesis de Valor para Proveedores:
Se propuso que "Si los proveedores tienen visibilidad de las solicitudes en tiempo real, podrán mejorar sus tiempos de respuesta y coordinación logística". La validación confirmó esta hipótesis, ya que los usuarios destacaron la importancia de recibir notificaciones inmediatas y contar con información actualizada para la toma de decisiones.

No obstante, se identificó que ofrecer únicamente información resumida no es suficiente; los usuarios requieren actualizaciones constantes y trazabilidad detallada de cada pedido, lo que valida la necesidad de integrar monitoreo en tiempo real como una funcionalidad central y no opcional.

**Bibliografia**

- Adzic, G. (s.f.). Impact Mapping. Recuperado de https://www.impactmapping.org/
- Brandolini, A. (s.f.). Introducing EventStorming. Recuperado de https://www.eventstorming.com/
- CareerFoundry. (s.f.). What are User Flows in User Experience (UX) Design?. Recuperado de https://careerfoundry.com/en/blog/ux-design/what-are-user-flows/
- Cohn, M. (s.f.). User Stories. Mountain Goat Software. Recuperado de https://www.mountaingoatsoftware.com/agile/user-stories
- Cone, M. (s.f.). The Markdown Guide. Recuperado de https://www.markdownguide.org/
- Conventional Commits. (s.f.). Conventional Commits. Recuperado de https://www.conventionalcommits.org/
- Cucumber. (s.f.). Gherkin Reference. Recuperado de https://cucumber.io/docs/gherkin/reference/
- Driessen, V. (2010). A successful Git branching model. nvie.com. Recuperado de https://nvie.com/posts/a-successful-git-branching-model/
- DZone. (s.f.). Acceptance Criteria in Scrum: Explanation, Examples, and Template. Recuperado de https://dzone.com/articles/acceptance-criteria-in-software-explanation-exampl
- Evans, E. (2004). Domain-Driven Design: Tackling Complexity in the Heart of Software. Addison-Wesley Professional. Recuperado de https://www.oreilly.com/library/view/domain-driven-design-tackling/0321125215/
- Fowler, M. (2006). Ubiquitous Language. Recuperado de https://martinfowler.com/bliki/UbiquitousLanguage.html
- Google. (s.f.). Google HTML/CSS Style Guide. Recuperado de https://google.github.io/styleguide/htmlcssguide.html
- Google. (s.f.). Google JavaScript Style Guide. Recuperado de https://google.github.io/styleguide/jsguide.html
- Gothelf, J., & Seiden, J. (2021). Lean UX: Designing Great Products with Agile Teams (3rd ed.). O'Reilly Media. Recuperado de https://www.oreilly.com/library/view/lean-ux-2nd/9781491953594/
- HubSpot. (s.f.). Full List of Meta Tags, Why They Matter for SEO & How to Write Them. Recuperado de https://blog.hubspot.com/marketing/meta-tags
- IBM Design. (s.f.). Empathy Map. Enterprise Design Thinking. Recuperado de https://www.ibm.com/design/thinking/page/toolkit/activity/empathy-map
- IBM Design. (s.f.). As-is Scenario Map. Enterprise Design Thinking. Recuperado de https://www.ibm.com/design/thinking/page/toolkit/activity/as-is-scenario-map
- Martin, R. C. (2017). Clean Architecture: A Craftsman's Guide to Software Structure and Design. Prentice Hall. Recuperado de https://www.oreilly.com/library/view/clean-architecture-a/9780134494272/
- Mendel, J. (s.f.). Seriously, what's your (startup's) problem?. Medium. Recuperado de https://medium.com/@jakemendel/seriously-whats-your-startup-s-problem-b3a884c54ab4
- Nielsen Norman Group. (1994). 10 Usability Heuristics for User Interface Design. Recuperado de https://www.nngroup.com/articles/ten-usability-heuristics/
- Nielsen Norman Group. (2016). The Four Dimensions of Tone of Voice. Recuperado de https://www.nngroup.com/articles/tone-of-voice-dimensions/
- Preston-Werner, T. (s.f.). Semantic Versioning 2.0.0. Recuperado de https://semver.org/
- Progressa Lean. (s.f.). 5W+2H - Técnica de análisis de problemas. Recuperado de https://www.progressalean.com/5w2h-tecnica-de-analisis-de-problemas/
- Refactoring.Guru. (s.f.). Design Patterns. Recuperado de https://refactoring.guru/es/design-patterns
- UXPressia. (s.f.). User vs. Buyer Persona: Differences and free template. Recuperado de https://uxpressia.com/blog/user-persona-vs-buyer-persona-difference
- Vernon, V. (2016). Domain-Driven Design Distilled. Addison-Wesley Professional. Recuperado de https://www.oreilly.com/library/view/domain-driven-design-distilled/9780134434964/
- Vernon, V. (s.f.). Domain-Driven Design Reference. Recuperado de https://domainlanguage.com/ddd/reference/

Anexos:

**Videos de Exposiciones:**
- **TB1:** [Enlace al video de la exposición del TB1 (Reemplazar con enlace real)](#)

Link del repositorio del informe: https://github.com/TechnoSAC/FullTank-Documents

Link del repositorio de la Landing Page:
https://github.com/TechnoSAC/Landing_Page

Link del repositorio del fronted:
https://github.com/TechnoSAC/frontend

Link del repositorio del backend:
https://github.com/TechnoSAC/backend

Link de los repositorios de la organización: https://github.com/TechnoSAC

Link del figma: https://www.figma.com/design/ZMHB35H60u2eUhctevkVKc/Fullank-Completo?node-id=0-1&t=I3nr2x0tcAinM7gE-1

URL de la Landing Page: https://technosac.github.io/FullTank_LandingPage/

Repositorio Landing: https://github.com/TechnoSAC/FullTank_LandingPage/settings/pages
