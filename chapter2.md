# Capítulo II: Requirements Elicitation & Analysis

## 2.1. Competidores

En el mercado existen diversas soluciones digitales enfocadas en la gestión de combustible y flotas que compiten de manera directa o indirecta con lo propuesto. Entre ellas destaca **Zavgar**, una plataforma SaaS que ayuda a las empresas con flotas vehiculares a optimizar costos y controlar el consumo de combustible. Otro competidor importante es **FuelCloud**, que ofrece una solución integrada de hardware y software para garantizar seguridad y precisión en el despacho de combustible, principalmente en empresas con tanques propios. Finalmente, **Wialon** se presenta como una plataforma internacional de gestión de flotas que combina monitoreo GPS, análisis operativos y control de combustible, dirigida a compañías logísticas y de transporte.

### 2.1.1. Análisis competitivo.

<table border="2">
  <tr>
    <th colspan="6" style="text-align:left">Competitive Analysis Landscape</th>
  </tr>
  <tr>
    <td colspan="1"><strong>¿Por qué llevar a cabo este análisis?</strong></td>
    <td colspan="5">Este análisis se está llevando a cabo porque queremos conocer las ventajas y desventajas de nuestra aplicación frente a la competencia, y cómo nos diferenciamos de ellas.</td>
  </tr>
  <tr>
    <td colspan="2"><strong></strong></td>
    <td><strong>FullTank</strong><br><img src="./assets/chapter-2/logo-FullTank.png" height="100"/></td>
    <td><strong>Zavgar</strong><br><img src="./assets/chapter-2/logo-zavgar.jpg" height="100"/></td>
    <td><strong>FuelCloud</strong><br><img src="./assets/chapter-2/logo-fuelcloud.jpg" height="100"/></td>
    <td><strong>Wialon</strong><br><img src="./assets/chapter-2/logo-wialon.jpg" height="100"/></td>
  </tr>

  <tr>
    <th rowspan="3">Perfil</th>
    <td><strong>Visión general</strong></td>
    <td>Plataforma web que digitaliza y estructura el proceso completo de pedido de combustible entre empresas y proveedores.</td>
    <td>SaaS para la gestión de consumo de combustible de flotas, con enfoque en eficiencia, monitoreo y costos.</td>
    <td>Solución con hardware/software para el control físico del despacho de combustible.</td>
    <td>Plataforma de gestión de flotas con control de combustible, GPS y reportes operativos.</td>
  </tr>
  <tr>
    <td><strong>Ventaja competitiva</strong></td>
    <td>Especialización en el flujo completo de pedido, despacho y análisis; integración de pagos y logística; UI intuitiva.</td>
    <td>No requiere hardware; ofrece métricas, control de gastos y reportes sobre consumo.</td>
    <td>Control físico preciso del combustible, monitoreo en tiempo real.</td>
    <td>Seguimiento en tiempo real, visualización de rutas, integración con sensores de combustible.</td>
  </tr>
  <tr>
    <td><strong>¿Qué valor ofrece al cliente?</strong></td>
    <td>Trazabilidad total, eficiencia operativa, reportes de consumo y validación segura de pedidos.</td>
    <td>Optimización de costos y control sobre el uso de combustible en flotas.</td>
    <td>Seguridad y precisión operativa en el control de combustible.</td>
    <td>Trazabilidad de flotas, alertas automáticas, análisis de rutas y consumo de combustible.</td>
  </tr>
  <tr>
    <th rowspan="2">Perfil de Marketing</th>
    <td><strong>Mercado objetivo</strong></td>
    <td>Empresas que solicitan combustible a proveedores.</td>
    <td>Empresas con flotas vehiculares que desean monitorear y reducir el consumo de combustible.</td>
    <td>Empresas con tanques de combustible propios.</td>
    <td>Empresas logísticas, distribuidoras y de transporte de combustible.</td>
  </tr>
  <tr>
    <td><strong>Estrategias de marketing</strong></td>
    <td>Alianzas con proveedores, demostraciones de ahorro, marketing de contenido enfocado en eficiencia.</td>
    <td>Enfoque digital, contenido técnico, integración con proveedores de tarjetas de combustible.</td>
    <td>Ferias industriales, distribuidores, venta consultiva entre empresas.</td>
    <td>Alianzas con distribuidores de GPS, marketing técnico, ferias de transporte.</td>
  </tr>
  <tr>
    <th rowspan="3">Perfil de Producto</th>
    <td><strong>Productos & Servicios</strong></td>
    <td>Plataforma para gestión completa de pedidos, seguimiento, reportes, validación y alertas.</td>
    <td>Plataforma web con módulo de abastecimiento, reportes de consumo, integración GPS y tarjetas.</td>
    <td>Hardware IoT y software para gestión, y control de combustible.</td>
    <td>Plataforma SaaS + app móvil con monitoreo, alertas, mapas y módulos personalizables.</td>
  </tr>
  <tr>
    <td><strong>Precios & Costos</strong></td>
    <td>Modelo SaaS con suscripción escalable según volumen y servicios.</td>
    <td>SaaS con modelos por flota activa o vehículos monitoreados.</td>
    <td>Venta e instalación de hardware + licencias de software.</td>
    <td>Modelo SaaS modular, basado en vehículos activos y funcionalidades activadas.</td>
  </tr>
  <tr>
    <td><strong>Canales de distribución</strong></td>
    <td>Web app responsive, potencial app móvil futura.</td>
    <td>Web app, marketing digital y comunidad de flotas.</td>
    <td>Plataforma web + hardware instalado en sitio.</td>
    <td>Red de partners global, distribuidores locales e integradores de sistemas GPS.</td>
  </tr>
  <tr>
    <th rowspan="4">Análisis SWOT</th>
    <td><strong>Fortalezas</strong></td>
    <td>Enfoque especializado, experiencia de usuario optimizada, integraciones clave, análisis avanzado de consumo.</td>
    <td>Implementación ágil, sin hardware, fácil adopción en empresas medianas.</td>
    <td>Control físico riguroso, solución probada en industrias exigentes.</td>
    <td>Plataforma robusta, cobertura internacional, integración con más de 2,400 dispositivos GPS.</td>
  </tr>
  <tr>
    <td><strong>Debilidades</strong></td>
    <td>Nueva en el mercado, menor reconocimiento de marca, necesita consolidar confianza.</td>
    <td>No gestiona el flujo completo del pedido, enfoque parcial en flotas.</td>
    <td>Alto costo, dependencia de hardware, menor adaptabilidad en mercados emergentes.</td>
    <td>No gestiona pedidos entre proveedor y solicitante, requiere configuración técnica inicial.</td>
  </tr>
  <tr>
    <td><strong>Oportunidades</strong></td>
    <td>Alta informalidad en el sector, digitalización creciente en logística, necesidad de trazabilidad y control.</td>
    <td>Mayor conciencia en eficiencia de flotas y digitalización de costos operativos.</td>
    <td>Nuevos mercados industriales con enfoque en seguridad y control.</td>
    <td>Creciente necesidad de control logístico y monitoreo de distribución en países en desarrollo.</td>
  </tr>
  <tr>
    <td><strong>Amenazas</strong></td>
    <td>Aparición de soluciones similares, resistencia al cambio en empresas tradicionales, competencia ERP.</td>
    <td>SaaS especializados con mayor cobertura funcional (ERP, proveedores, logística).</td>
    <td>SaaS ágiles y sin hardware físico, que ofrecen soluciones más accesibles.</td>
    <td>SaaS más específicos y ligeros, enfocados exclusivamente en la trazabilidad de entregas.</td>
  </tr>
</table>

### 2.1.2. Estrategias y tácticas frente a competidores.

**TechnoSAC** aplicará diversas estrategias para afrontar la competencia y aprovechar las oportunidades que ofrece el sector.

#### a. Diferenciación a través de especialización
Una de las principales estrategias de **TechnoSAC** es la **especialización en el flujo completo de pedido de combustible**. A diferencia de soluciones como **Zavgar**, que están orientadas principalmente al control y análisis del consumo de combustible en flotas, nuestra plataforma se enfoca en las **interacciones B2B** entre empresas solicitantes y proveedores. Esto nos permite ofrecer un control dedicado del pedido, gestión de la logística, y reportes detallados de consumo y entregas, lo cual no está presente en la mayoría de las plataformas competidoras.

- **Táctica**: Desarrollar funcionalidades para la validación automática de pagos, gestión de stock en tiempo real y la optimización del transporte logrando la automatización de procesos que solo eran logrados de forma manual. Esto crea una ventaja frente a competidores como **FuelCloud**, que se centran más en el control físico del combustible y menos en la administración a nivel operativo.

#### b. Innovación en la interfaz de usuario y experiencia

El sistema de **TechnoSAC** está diseñado para ofrecer una **experiencia de usuario optimizada**, algo que **Wialon**, **FuelCloud** y la propia **OSINERGMIN** no abordan en sus plataformas. Al ser una solución especializada y dirigida a una tarea específica, podemos dedicar más recursos en crear una interfaz intuitiva y procesos bien definidos brindando comodidad y seguridad a nuestros usuarios.

- **Táctica**: Diseñar una **interfaz intuitiva y consistente** que permita a los usuarios acceder a reportes de consumo, validar pedidos y coordinar logística con facilidad. Además, ofrecer **soporte y formación continua** para asegurar que los usuarios aprovechen al máximo todas las funcionalidades del sistema.

#### c. Flexibilidad en precios y modelo SaaS escalable
El modelo de precios de **TechnoSAC** ofrece **planes escalables basados en suscripción**, lo que hace que sea más accesible para medianas y grandes empresas. Esto es más competitivo frente a **Wialon**, que puede no ser una opción viable para empresas que solo requieren una solución de pedidos de combustible. También es más asequible que **FuelCloud**, que requiere una inversión considerable en hardware, instalación y mantenimiento.

- **Táctica**: Ofrecer un modelo de suscripción flexible y **precios competitivos**, con **múltiples niveles de suscripción** adaptados a las necesidades de diferentes empresas. Esto permitirá que empresas de menor tamaño puedan acceder a la plataforma sin comprometer su presupuesto, a la vez que se asegura el crecimiento a largo plazo a medida que la empresa crece.

#### d. Aprovechamiento de la digitalización en la logística
El sector de la logística está experimentando una transformación digital acelerada. **TechnoSAC** se aprovechará de esta tendencia buscando la integración de la plataforma con otras soluciones logísticas (como los sistemas de gestión de vehículos o flotas). De esta forma podemos ofrecer una solución más completa y eficiente.

- **Táctica**: Colaborar con empresas de **gestión de flotas** para optimizar el proceso de asignación de vehículos, cisternas y choferes. También se considerará la posibilidad de integrar **sensores IoT** en los camiones de reparto para un control más preciso sobre el combustible transportado y la entrega.

#### e. Expansión hacia mercados internacionales
Si bien **TechnoSAC** está inicialmente orientada a empresas locales, el modelo de negocio y la flexibilidad de la plataforma la hacen ideal para expandirse a **mercados internacionales**. Competidores como **Wialon** ya tienen presencia en mercados globales, pero su enfoque en empresas grandes y sus altos costos de implementación pueden ser una barrera para empresas de menor tamaño, limitando su alcance.

- **Táctica**: Iniciar la expansión en mercados emergentes donde la digitalización en la logística es una necesidad creciente. Esto incluirá la **localización de la plataforma** (idioma, moneda, regulaciones locales) para facilitar la adaptabilidad de los nuevos mercados.

## 2.2. Entrevistas.

### 2.2.1. Diseño de entrevistas.

**A. Proveedores de Combustible**

**Preguntas:**

1. ¿Cuál es su cargo dentro de la empresa proveedora?
2. ¿Qué tipos de clientes atienden principalmente (logística, construcción, minería, agroindustria)?
3. ¿Qué volumen de operaciones realizan mensualmente?
4. ¿Cómo gestionan actualmente los pedidos y contratos de sus clientes?
5. ¿Qué problemas han experimentado con los métodos tradicionales (llamadas, correos, planillas)?
6. ¿Utilizan algún software especializado para ventas o logística? 
7. ¿Qué características valoraría más en una plataforma digital para gestionar pedidos?
8. ¿Considera que una solución que centralice cotizaciones, contratos y entregas sería útil para su empresa?
9. ¿Qué tan importante es para ustedes tener reportes históricos y comparativos de ventas?
10. ¿Qué estrategias usan actualmente para fidelizar clientes, y cómo cree que una plataforma como NombredelaStartup podría apoyarlos?

---

**B. Empresas Solicitantes**

**Preguntas:**

1. ¿Cuál es su cargo en la empresa? 
2. ¿Hace cuánto tiempo trabaja en el sector energético/logístico? 
3. ¿Qué volumen de combustible gestionan aproximadamente al mes? 
4. ¿Cómo gestionan actualmente la compra y control de combustible? 
5. ¿Qué herramientas usan (Excel, llamadas, correos, sistemas propios)? 
6. ¿Cuáles son los principales problemas que enfrentan con su sistema actual?
7. ¿Qué tan importante es para usted contar con trazabilidad en tiempo real? 
8. ¿Qué dispositivos utilizan para gestionar pedidos (PC, móvil, tablet)? 
9. ¿Qué información considera más valiosa al momento de comprar combustible (precio, tiempo de entrega, historial de proveedor, etc.)? 
10. ¿Cómo afecta la falta de transparencia en los precios a sus decisiones de compra? 
11. ¿Le interesaría recibir notificaciones en tiempo real sobre cambios de precio o estado de sus pedidos? 
12. ¿Qué barreras considera que dificultarían implementar una solución digital como NombredelaStartup en su empresa?

### 2.2.2 Registro de entrevistas
**1. Segmento 1: Empresas solicitantes de combustible**
- Entrevista 1:
  - Nombre: Kevyn Anthony Asto Jacome
  - Edad: 32
  - Distrito: San Miguel
<div allign="center">

  <img src="assets/chapter-2/kevyn.png" alt="Captura primer entrevistado"/> 
  <p>Link de la entrevista: https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241c630_upc_edu_pe/IQCKV9lpC3LTSYq8V0HBefpVAS_fcsy2aqA-XEwNtES_c3g?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=uQEHe9</p>
</div>

- Entrevista 2:
  - Nombre: Renato Guillermo Calvo Yalan
  - Edad: 22 años
  - Distrito: San Juan de Lurigancho, Lima
<div allign="center">
<img src="assets/chapter-2/Renato.png" alt="Captura segundo entrevistado"/>

  <p>Link de la entrevista: https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241c630_upc_edu_pe/IQDS2Yop64CbRLtW82ISOuc4AU56u40anOCvBotRFMydvE4?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=Jgu6ZG</p>
</div>

- Entrevista 2:
  - Nombre: Alessando Daniel Bravo Castillo
  - Edad: 24 años
  - Distrito: San Martin de Porres, Lima
<div allign="center">
<img src="assets/chapter-2/Alessandro.png" alt="Captura tercero entrevistado"/>
  
  <p>Link de la entrevista: https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241c630_upc_edu_pe/IQA6kFOl51ZHR64XnqKoMLX5AZqcLey9f3T7M8bFaGsdJZA?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=kvkkFZ</p>
</div>


**2. Segmento 2: Proveedores de combustible**
- Entrevista 1:
  - Nombre: Francesco
  - Edad: 20 años
  - Distrito: La Molina, Lima
<div allign="center">
<img src="assets/chapter-2/Francesco.png" alt="Captura entrevistado Francesco"/>
<p>Link de la entrevista: https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241c630_upc_edu_pe/IQDS2Yop64CbRLtW82ISOuc4AU56u40anOCvBotRFMydvE4?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=0GD1zP</p>
</div>

- Entrevista 2:
  - Nombre: Samuel
  - Edad: 48 años
  - Distrito: Bellavista, Lima
<div allign="center">
<img src="assets/chapter-2/Samuel.png" alt="Captura entrevistado Samuel"/>
<p>Link de la entrevista: https://upcedupe-my.sharepoint.com/:v:/g/personal/u20241c630_upc_edu_pe/IQCHmDhpE9SeS79-7cpkvvj4ARv-HzcyTjlnuszQWkBofBQ?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=DSF66n</p>
</div>

### 2.2.3 Análisis de entrevistas

## 2.3 Needfinding
### 2.3.1 User Personas
-Segmento 1: Empresas solicitantes de combustible

-Segmento 2: Proveedores de Combustible

### 2.3.2 User Task Matrix
-Segmento 1: Empresas solicitantes de combustible
<table border="1">
  <thead>
    <tr>
      <th>Tarea</th>
      <th>Descripción</th>
      <th>Frecuencia</th>
      <th>Importancia</th>
      <th>Dolor actual (Pain Point)</th>
      <th>Oportunidad de mejora</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Registrar pedido de combustible</td>
      <td>Ingresar cantidad, tipo y fecha de entrega</td>
      <td>Alta</td>
      <td>Alta</td>
      <td>Procesos manuales y propensos a errores</td>
      <td>Formulario digital rápido (&lt;3 min)</td>
    </tr>
    <tr>
      <td>Consultar estado del pedido</td>
      <td>Verificar estado del pedido</td>
      <td>Alta</td>
      <td>Alta</td>
      <td>Falta de trazabilidad, requiere llamadas</td>
      <td>Tracking en tiempo real</td>
    </tr>
    <tr>
      <td>Modificar pedido</td>
      <td>Editar detalles antes de confirmación</td>
      <td>Media</td>
      <td>Alta</td>
      <td>Dificultad para hacer cambios</td>
      <td>Edición simple con historial</td>
    </tr>
    <tr>
      <td>Comunicarse con proveedor</td>
      <td>Coordinar detalles del pedido</td>
      <td>Alta</td>
      <td>Alta</td>
      <td>Uso de múltiples canales</td>
      <td>Chat integrado</td>
    </tr>
    <tr>
      <td>Revisar historial de pedidos</td>
      <td>Consultar pedidos anteriores</td>
      <td>Media</td>
      <td>Media</td>
      <td>Información dispersa</td>
      <td>Historial centralizado</td>
    </tr>
    <tr>
      <td>Recibir notificaciones</td>
      <td>Alertas sobre estado del pedido</td>
      <td>Alta</td>
      <td>Alta</td>
      <td>Seguimiento manual</td>
      <td>Notificaciones automáticas</td>
    </tr>
    <tr>
      <td>Generar reportes</td>
      <td>Analizar consumo de combustible</td>
      <td>Baja</td>
      <td>Media</td>
      <td>Falta de datos estructurados</td>
      <td>Dashboard con métricas</td>
    </tr>
  </tbody>
</table>


-Segmento 2: Proveedores de Combustible


<table border="1">
  <thead>
    <tr>
      <th>Tarea</th>
      <th>Descripción</th>
      <th>Frecuencia</th>
      <th>Importancia</th>
      <th>Dolor actual (Pain Point)</th>
      <th>Oportunidad de mejora</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Recibir pedidos</td>
      <td>Visualizar solicitudes de clientes</td>
      <td>Alta</td>
      <td>Alta</td>
      <td>Pedidos por múltiples canales</td>
      <td>Bandeja centralizada</td>
    </tr>
    <tr>
      <td>Validar pedidos</td>
      <td>Confirmar disponibilidad</td>
      <td>Alta</td>
      <td>Alta</td>
      <td>Falta de organización</td>
      <td>Flujo estructurado</td>
    </tr>
    <tr>
      <td>Programar entregas</td>
      <td>Asignar fechas y logística</td>
      <td>Alta</td>
      <td>Alta</td>
      <td>Coordinación manual compleja</td>
      <td>Sistema de planificación</td>
    </tr>
    <tr>
      <td>Actualizar estado del pedido</td>
      <td>Marcar progreso del pedido</td>
      <td>Alta</td>
      <td>Alta</td>
      <td>Información desactualizada</td>
      <td>Actualización en tiempo real</td>
    </tr>
    <tr>
      <td>Gestionar múltiples pedidos</td>
      <td>Organizar pedidos simultáneos</td>
      <td>Alta</td>
      <td>Alta</td>
      <td>Sobrecarga operativa</td>
      <td>Panel de control</td>
    </tr>
    <tr>
      <td>Comunicarse con clientes</td>
      <td>Resolver dudas y coordinar</td>
      <td>Alta</td>
      <td>Alta</td>
      <td>Exceso de llamadas</td>
      <td>Chat integrado</td>
    </tr>
    <tr>
      <td>Monitorear desempeño</td>
      <td>Evaluar eficiencia</td>
      <td>Media</td>
      <td>Media</td>
      <td>Falta de métricas</td>
      <td>Dashboard analítico</td>
    </tr>
  </tbody>
</table>


### 2.3.3 User Journey Mapping


-Segmento 1: Empresas solicitantes de combustible


<table border="1">
  <thead>
    <tr>
      <th>Etapa</th>
      <th>Acciones</th>
      <th>Pensamientos</th>
      <th>Emociones</th>
      <th>Pain Points</th>
      <th>Oportunidades</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Identificación de necesidad</td>
      <td>Detecta que necesita combustible</td>
      <td>“Necesito hacer el pedido rápido”</td>
      <td>😐 Neutral</td>
      <td>No hay sistema centralizado</td>
      <td>Recordatorios automáticos</td>
    </tr>
    <tr>
      <td>Registro del pedido</td>
      <td>Contacta al proveedor (WhatsApp/correo)</td>
      <td>“Espero no equivocarme en los datos”</td>
      <td>😕 Estrés</td>
      <td>Errores manuales</td>
      <td>Formulario digital guiado</td>
    </tr>
    <tr>
      <td>Confirmación</td>
      <td>Espera respuesta del proveedor</td>
      <td>“¿Habrá sido recibido?”</td>
      <td>😟 Incertidumbre</td>
      <td>Falta de confirmación inmediata</td>
      <td>Confirmación automática</td>
    </tr>
    <tr>
      <td>Seguimiento</td>
      <td>Hace llamadas para saber estado</td>
      <td>“Necesito saber dónde está”</td>
      <td>😤 Frustración</td>
      <td>No hay tracking</td>
      <td>Seguimiento en tiempo real</td>
    </tr>
    <tr>
      <td>Recepción</td>
      <td>Recibe el combustible</td>
      <td>“Espero que llegue a tiempo”</td>
      <td>🙂 Alivio</td>
      <td>Retrasos inesperados</td>
      <td>Alertas de entrega</td>
    </tr>
    <tr>
      <td>Post-servicio</td>
      <td>Registra o revisa el pedido</td>
      <td>“Necesito llevar control”</td>
      <td>😐 Neutral</td>
      <td>Datos desorganizados</td>
      <td>Historial automático</td>
    </tr>
  </tbody>
</table>


-Segmento 2: Proveedores de Combustible


<table border="1">
  <thead>
    <tr>
      <th>Etapa</th>
      <th>Acciones</th>
      <th>Pensamientos</th>
      <th>Emociones</th>
      <th>Pain Points</th>
      <th>Oportunidades</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Recepción de pedido</td>
      <td>Recibe pedidos por múltiples canales</td>
      <td>“Tengo demasiados pedidos por revisar”</td>
      <td>😓 Estrés</td>
      <td>Desorganización</td>
      <td>Bandeja centralizada</td>
    </tr>
    <tr>
      <td>Validación</td>
      <td>Verifica datos del pedido</td>
      <td>“¿Está todo correcto?”</td>
      <td>😐 Neutral</td>
      <td>Errores en información</td>
      <td>Validación automática</td>
    </tr>
    <tr>
      <td>Planificación</td>
      <td>Organiza rutas y entregas</td>
      <td>“Esto toma mucho tiempo”</td>
      <td>😫 Carga</td>
      <td>Proceso manual</td>
      <td>Optimización de rutas</td>
    </tr>
    <tr>
      <td>Comunicación</td>
      <td>Coordina con clientes</td>
      <td>“Recibo demasiadas llamadas”</td>
      <td>😤 Frustración</td>
      <td>Saturación de comunicación</td>
      <td>Notificaciones automáticas</td>
    </tr>
    <tr>
      <td>Entrega</td>
      <td>Realiza despacho</td>
      <td>“Debe salir todo bien”</td>
      <td>😬 Tensión</td>
      <td>Falta de visibilidad</td>
      <td>Tracking en tiempo real</td>
    </tr>
    <tr>
      <td>Evaluación</td>
      <td>Revisa desempeño</td>
      <td>“¿Estamos siendo eficientes?”</td>
      <td>🤔 Reflexión</td>
      <td>No hay métricas claras</td>
      <td>Dashboard analítico</td>
    </tr>
  </tbody>
</table>




### 2.3.4 Empathy Mapping


-Segmento 1: Empresas solicitantes de combustible



-Segmento 2: Proveedores de Combustible



## 2.4 Big Picture Event Storming


## 2.5 Ubiquitous Language
