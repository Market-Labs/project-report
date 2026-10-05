# Capítulo I: Introducción

## 1.1. Startup Profile

### 1.1.1. Descripción de la Startup

Market-Labs es una startup tecnológica peruana de reciente creación, orientada al desarrollo de iniciativas empresariales basadas en tecnología e innovación. La organización nace con el propósito de identificar oportunidades de mejora en actividades comerciales y operativas, transformándolas en propuestas de valor que puedan generar beneficios económicos, sociales y ambientales.

Como empresa emergente, Market-Labs adopta un enfoque de innovación continua, característico de las startups, buscando validar sus ideas de negocio de manera progresiva y adaptarse a las necesidades de su mercado objetivo. Su modelo de desarrollo se basa en la identificación de problemas reales, la experimentación y la mejora constante de sus propuestas, priorizando la generación de valor antes que el crecimiento basado únicamente en estructuras empresariales tradicionales. En este sentido, Market-Labs aspira a consolidarse progresivamente como una empresa tecnológica capaz de identificar nuevas oportunidades de negocio y desarrollar propuestas innovadoras que respondan a necesidades concretas del mercado. Su crecimiento se plantea mediante la generación de productos y servicios digitales escalables, procurando establecer relaciones sostenibles con sus clientes y demás actores relacionados con sus actividades empresariales.

**Misión:** Desarrollar iniciativas tecnológicas innovadoras que permitan atender necesidades reales del mercado, generando valor para los usuarios y contribuyendo al desarrollo de actividades empresariales más eficientes y sostenibles.

**Visión:** Consolidarse como una startup tecnológica peruana reconocida por su capacidad de innovación, adaptación y generación de propuestas digitales escalables que respondan a los nuevos desafíos del mercado.

**Valores:** Innovación, eficiencia, sostenibilidad, transparencia, adaptabilidad y orientación al usuario.

### 1.1.2. Perfiles de integrantes del equipo

| Imagen | Apellidos y nombres | Código | Carrera | Perfil |
|:---:|:---|:---:|:---|:---|
| <img src="assets/chapter-01/profile_caceres.png" alt="Foto de Albino Caceres" width="120" /> | **Cáceres Pizarro, Albino Florencio** | U201923820 | Ingeniería de Software | Me considero una persona responsable y proactiva que le gusta trabajar en equipo. Además, siempre estoy abierto a ayudar, en lo posible, a cualquier integrante del equipo. Además, busco adaptarme rápidamente a los diversos retos que se presentan en el ciclo. |
|<img src="assets/chapter-01/profile_winnieMerino.jpg" alt="Foto de Winnie Merino" width="120" /> | **Merino Ordinola, Winnie Lisbeth** | U20231E504 | Ingeniería de Software | Estudiante de la carrera de Ingeniería de Software. Mis principales destrezas son las habilidades para trabajar en equipo, la creatividad y la investigación. Mi mayor interés es tanto proponer ideas innovadoras que solucionen problemas cercanos en nuestra realidad, como llevarlas a cabo a través del software. |
| <img src="assets/chapter-01/Sebastian.png" alt="Foto de Andre Sebastian" width="120" /> | **Quispe Almonacid, Andre Sebastian** | U201815005 | Ingeniería de Software | Me considero una persona analítica, constante y apasionada por la tecnología. Tengo un fuerte interés en la gestión de bases de datos, la estructura de los sistemas y el desarrollo de software. Disfruto entendiendo cómo funcionan las cosas desde la raíz y transformando la lógica en soluciones limpias y eficientes. Mi meta es seguir creciendo en el campo tecnológico y consolidarme como una profesional capaz de conectar bases de datos sólidas con el desarrollo moderno. |
| <img src="assets/chapter-01/profile_huaranga.jpg" alt="Foto de Matias Huaranga" width="120" /> | **Huaranga Romero, Matias Daniel** | U202410746 | Ingeniería de Software | Estudiante de Ingeniería de Software, responsable, proactivo y orientado al trabajo en equipo. Me destaco por mi creatividad, capacidad de investigación y disposición constante para apoyar a mis compañeros. Apasionado por transformar problemas reales en soluciones innovadoras a través del software, con una rápida adaptación frente a nuevos retos académicos y profesionales. |
| <img src="assets/chapter-01/profile_torres.png" alt="Foto de Alexis Torres" width="120" /> | **Torres Huaman, Alexis Calín** | U20241G152 | Ingeniería de Software | Estudiante de Ingeniería de Software. Me considero una persona comprometida, analítica y apasionada por la resolución de problemas mediante el uso de la tecnología. Destaco por mi habilidad para trabajar en equipo, investigar nuevas herramientas y proponer ideas innovadoras que optimicen el desarrollo de software dentro del proyecto. |

---

## 1.2. Solution Profile

Nuestra solución, MarketGo, es una plataforma web orientada a la gestión, conservación y abastecimiento de productos orgánicos. La solución conecta a administradores de minimarkets y proveedores dentro de un mismo ecosistema digital, permitiendo administrar inventarios, lotes, pedidos, entregas y condiciones de almacenamiento desde una plataforma centralizada.

La plataforma utiliza un dashboard común para ambos segmentos, pero aplica diferentes permisos de acuerdo con el rol del usuario. Los administradores de minimarkets cuentan con permisos de lectura y escritura sobre la información de su operación, mientras que los proveedores disponen de permisos de consulta y acciones específicas relacionadas con la generación de pedidos, sin poder modificar directamente el inventario del minimarket.

Para los administradores de minimarkets, la plataforma permite controlar el inventario propio, gestionar lotes y fechas de vencimiento, monitorear las condiciones ambientales de almacenamiento, recibir alertas sobre productos en riesgo y gestionar procesos de merma o donación. Asimismo, pueden consultar la disponibilidad de productos ofrecidos por los proveedores, realizar pedidos de abastecimiento y aceptar o rechazar los pedidos generados. Cuando un pedido es aceptado, los productos correspondientes se incorporan automáticamente al inventario del minimarket.

Para los proveedores, la plataforma permite consultar los productos que ofrecen y su disponibilidad, generar pedidos de abastecimiento dirigidos a los minimarkets y consultar el estado de las operaciones realizadas. Los proveedores no pueden modificar directamente el inventario del minimarket, ya que cualquier incorporación de productos depende de la aceptación del pedido por parte del administrador.

La solución busca reducir las pérdidas asociadas al deterioro de productos orgánicos y mejorar la coordinación entre compradores y proveedores mediante información centralizada, trazabilidad y un sistema de permisos que controla las acciones disponibles para cada segmento.

### 1.2.1. Antecedentes y problemática

Los productos orgánicos y alimentos frescos presentan una alta sensibilidad a factores como la temperatura, humedad, manipulación y tiempo de almacenamiento. Cuando estas condiciones no son controladas adecuadamente, aumenta el riesgo de deterioro y, como consecuencia, pueden generarse pérdidas económicas, desperdicio de alimentos y disminución de la disponibilidad de productos para los consumidores.

En los minimarkets, uno de los principales desafíos consiste en mantener un control adecuado sobre los productos almacenados, sus lotes y fechas de vencimiento. La ausencia de mecanismos centralizados de seguimiento puede dificultar la identificación temprana de productos en riesgo y provocar que estos sean detectados cuando ya no pueden comercializarse.

A esta problemática se suma la necesidad de mantener condiciones apropiadas de conservación. El monitoreo manual o fragmentado de variables como temperatura y humedad limita la capacidad de los responsables del establecimiento para identificar oportunamente situaciones anómalas que puedan afectar determinados productos.

Por otro lado, el abastecimiento representa un segundo desafío. Los administradores de minimarkets necesitan conocer qué productos y lotes se encuentran disponibles para realizar pedidos oportunamente, mientras que los proveedores necesitan disponer de un mecanismo que les permita generar pedidos y consultar el estado de las operaciones relacionadas con los productos que ofrecen.

Esta situación genera una fragmentación de información entre inventarios, pedidos, entregas e incidencias. La utilización de herramientas no especializadas puede dificultar la coordinación entre ambas partes y aumentar el riesgo de errores, retrasos y pérdidas de productos.

Ante este escenario, se propone una plataforma digital que centralice la información de inventarios, lotes, conservación y abastecimiento, conectando a los administradores de minimarkets y proveedores mediante un dashboard común y un sistema de permisos que limite las acciones de acuerdo con el rol de cada usuario.

**Técnica "The 5W's y 2H's" aplicada al problema:**

| The 5W's y 2H's | Pregunta | Descripción |
|:---|:---|:---|
| **Who** | ¿Quiénes están involucrados? | Administradores de minimarkets responsables de la comercialización y abastecimiento de productos orgánicos, y proveedores encargados de ofrecer y distribuir dichos productos. |
| **What** | ¿Cuál es el problema? | Dificultad para gestionar de manera integrada el inventario, conservación, lotes, vencimientos y abastecimiento de productos orgánicos, generando riesgo de pérdidas y desabastecimiento. |
| **Where** | ¿Dónde ocurre? | Principalmente en los procesos de almacenamiento y comercialización de productos orgánicos en minimarkets, así como en la gestión de pedidos y abastecimiento entre minimarkets y proveedores. |
| **When** | ¿Cuándo sucede? | Durante el almacenamiento, seguimiento de lotes, control de fechas de vencimiento y procesos de abastecimiento, pedidos y recepción de productos. |
| **Why** | ¿Por qué sucede? | Debido a la fragmentación de la información, utilización de procesos manuales y ausencia de una plataforma especializada que conecte inventario, conservación y abastecimiento. |
| **How** | ¿Cómo se manifiesta? | Mediante dificultades para identificar productos en riesgo, controlar lotes y vencimientos, conocer disponibilidad de productos, realizar pedidos y dar seguimiento a las operaciones de abastecimiento. |
| **How Much** | ¿Cuánto impacto tiene? | El problema puede traducirse en pérdidas económicas por productos deteriorados o vencidos, desperdicio de alimentos, interrupciones en el abastecimiento y mayores costos operativos. |

---

### 1.2.2. Lean UX Process.

#### 1.2.2.1. Lean UX Problem Statements.
En el mercado peruano, los administradores de minimarkets que comercializan productos orgánicos necesitan controlar inventarios, lotes, vencimientos y condiciones de almacenamiento para evitar mermas y reponer a tiempo. Las entrevistas muestran el uso combinado de POS, hojas de cálculo, libretas y mensajería; esa dispersión dificulta detectar productos en riesgo y conocer el stock disponible. Los proveedores, por su parte, necesitan mantener actualizados su catálogo, lotes y disponibilidad, y dar seguimiento a los pedidos de los minimarkets, pero la coordinación mediante archivos y conversaciones separadas dificulta confirmar cantidades, cambios y estados de pedido.

Existen soluciones de gestión comercial e inventario revisadas en el análisis competitivo, pero cada una cubre solo una parte del proceso. La oportunidad de **MarketLabs** es atender de forma integrada la conservación de productos orgánicos, la trazabilidad por lotes y la coordinación de pedidos entre ambos segmentos. A partir de estos hallazgos y del análisis 5W+2H, el Problem Statement se redactó con la plantilla oficial de Lean UX para una iniciativa nueva (*brand new initiative*):


> **The current state of** organic product retail in Lima's minimarkets has focused primarily on manual and fragmented control: minimarket administrators track inventory, batches, expiration dates and storage conditions through physical checks, notebooks, POS systems and spreadsheets, while organic product suppliers receive and confirm replenishment orders through WhatsApp messages and phone calls. As a result, products expire or spoil before they are detected, stock records become inaccurate after orders are transcribed manually, and both parties lose time confirming the status of each delivery. In Peru, about 12.8 million tons of food are lost every year, 47.6% of the annual food supply (OECD, 2025).
>
> **What existing products/services fail to address is** the connection between replenishment and the minimarket's internal control. FreshTracker covers storage monitoring, ShelfLife covers inventory and expiration tracking, and Peru Marketplace connects buyers and suppliers, but none of them links a supplier's shipment to the minimarket's inventory, batches and storage alerts in a single flow with role-based permissions for both parties.
>
> **Our product/service will address this gap by** offering MarketGo, a responsive SaaS web platform where minimarket administrators manage inventory, batches, expirations and storage conditions with automatic alerts, and create replenishment orders that suppliers accept and fulfill through shipping orders. Once the administrator accepts a shipping order, the received products and batches are automatically added to the minimarket's inventory, and both parties follow the status of each operation from role-based dashboards.
>
> **Our initial focus will be** small and medium organic minimarkets in Metropolitan Lima, represented by the persona Russell Estrada, and the organic product suppliers and distributors that serve them, represented by the persona Marco Antonio Ríos.
>
> **We'll know we are successful when we see:**
> - A 30% reduction in products written off due to expiration or spoilage in subscribed minimarkets within the first 6 months.
> - The average time between the creation of a replenishment order and the generation of its shipping order reduced from 24 hours to less than 4 hours in 80% of orders during the first semester.
> - 100% of accepted shipping orders updating the minimarket's inventory without manual entry.
> - At least 20 active minimarkets and 5 active suppliers using the platform weekly by the end of the first semester.

**Restricciones (constraints) consideradas:**

- El MVP se desarrolla como aplicación web responsive (Landing Page, Web Application y RESTful API), sin aplicación móvil nativa.
- El monitoreo de temperatura y humedad utiliza datos simulados en la etapa inicial; la integración con sensores físicos queda fuera del alcance inicial.
- La plataforma no procesa pagos ni facturación electrónica; las condiciones comerciales se acuerdan fuera de MarketGo.
- El proveedor no puede modificar el inventario del minimarket: toda incorporación de productos depende de que el administrador acepte la orden de envío.
- El alcance geográfico inicial es Lima Metropolitana.


**Relación del Problem Statement con el análisis 5W+2H:**

| Elemento de la plantilla | Resultado 5W+2H que lo sustenta |
|---|---|
| The current state of… | **Who**, **Where** y **When**: administradores y proveedores, durante el almacenamiento, el control de lotes y el abastecimiento. |
| What existing products/services fail to address… | **Why**: fragmentación de la información y ausencia de una plataforma que integre inventario, abastecimiento y monitoreo. |
| Our product/service will address this gap by… | **What** y **How**: gestión integrada de inventario, lotes, vencimientos, conservación, pedidos y órdenes de envío. |
| Our initial focus will be… | **Who** y **Where**: minimarkets orgánicos y proveedores de Lima Metropolitana. |
| We'll know we are successful when we see… | **How Much**: pérdidas por mermas, desabastecimiento y costos operativos, convertidos en métricas cuantitativas. |


1. **Domain:** Gestión logística, abastecimiento y monitoreo de productos orgánicos.

2. **Customer Segments:** Administradores de minimarkets y proveedores de productos orgánicos.

3. **Pain Points:** Pérdidas por deterioro o vencimiento, falta de visibilidad sobre las condiciones de almacenamiento, dificultades para controlar niveles de stock, lotes y vencimientos, problemas para consultar disponibilidad de productos y coordinar pedidos de abastecimiento.

4. **Gap:** Las soluciones comerciales comparadas cubren por separado la conservación, el inventario o la conexión B2B; la oportunidad identificada es integrar la conservación de productos orgánicos, la trazabilidad por lotes y el flujo de pedidos y órdenes de envío entre minimarket y proveedor, con permisos diferenciados para modificar el inventario.

5. **Vision/Strategy:** Centralizar la información operativa para identificar riesgos, anticipar necesidades de reposición, gestionar inventarios y facilitar el abastecimiento mediante un flujo en el que el administrador crea el pedido, el proveedor lo atiende con una orden de envío y el administrador acepta la recepción antes de actualizar el inventario.

6. **Initial Segment:** Administradores de minimarkets orgánicos de Lima Metropolitana y los proveedores de productos orgánicos que los abastecen.

---

#### 1.2.2.2. Lean UX Assumptions.

**Business Assumptions:**

1. Se considera que los administradores de minimarkets necesitan mejorar el control de sus productos orgánicos para reducir pérdidas asociadas al deterioro y vencimiento.

2. Se plantea que una plataforma centralizada puede mejorar la visibilidad sobre inventarios, niveles de stock, lotes, vencimientos y condiciones de almacenamiento.

3. Se considera que los proveedores necesitan una herramienta especializada para gestionar productos, disponibilidad, lotes y pedidos de abastecimiento dirigidos a diferentes minimarkets.

4. Se asume que la integración entre minimarkets y proveedores permitirá mejorar la eficiencia del proceso de abastecimiento.

5. Se considera que las alertas de temperatura y humedad permitirán identificar oportunamente condiciones que puedan afectar la conservación de los productos.

6. Se plantea que la centralización de los pedidos permitirá mejorar la trazabilidad de las operaciones de abastecimiento.

7. Se estima que un modelo SaaS puede facilitar el acceso de pequeñas y medianas empresas a las funcionalidades de la plataforma sin requerir infraestructura tecnológica propia.

8. Se considera que la principal diferenciación de la solución será integrar la gestión de inventarios, abastecimiento y monitoreo de las condiciones de almacenamiento de productos orgánicos.

9. Se asume que los datos de monitoreo IoT pueden ser simulados durante la etapa inicial para validar los flujos funcionales sin depender de dispositivos físicos.

10. Se asume que la plataforma podrá evolucionar posteriormente para incorporar sensores IoT reales y capacidades analíticas más avanzadas.

11. Se presume que uno de los principales riesgos de adopción será la resistencia de los usuarios a reemplazar procesos manuales y herramientas informales.

12. Se plantea que una interfaz sencilla y dashboards diferenciados permitirán reducir la complejidad para cada tipo de usuario.

13. Se considera que la viabilidad del producto dependerá de que los beneficios obtenidos mediante la reducción de pérdidas y mejora del abastecimiento sean percibidos como superiores al costo de la solución.


**Business Outcome Assumptions**

1. Reducir la cantidad de productos dados de baja como consecuencia de condiciones inadecuadas de almacenamiento o vencimiento.

2. Incrementar la trazabilidad de los productos, lotes y fechas de vencimiento gestionados por los minimarkets.

3. Reducir el tiempo necesario para identificar productos o lotes que puedan encontrarse en condiciones de riesgo.

4. Mejorar la capacidad de los administradores para anticipar necesidades de reposición mediante información sobre niveles de stock.

5. Mejorar la disponibilidad de información para la toma de decisiones relacionadas con el abastecimiento.

6. Incrementar la trazabilidad de los pedidos desde su creación por parte del administrador hasta la recepción de la orden de envío y la actualización del inventario.

7. Incrementar la captación de nuevos minimarkets y proveedores que se registran en la plataforma a partir de la Landing Page.

Estos resultados se evaluarán, respectivamente, mediante la cantidad de productos dados de baja por vencimiento o deterioro; el porcentaje de productos con lote y vencimiento registrados; el tiempo para identificar productos en riesgo; el tiempo entre la detección de stock bajo y la decisión de reposición; la disponibilidad de información vigente sobre productos y pedidos; y el porcentaje de pedidos con estado e historial de decisiones consultables. Se compararán con una línea base levantada durante las pruebas con usuarios.


**User Assumptions**

1. Los administradores de minimarkets necesitan visualizar rápidamente el estado de su inventario y los productos próximos a vencer.

2. Los administradores de minimarkets necesitan identificar productos con niveles de stock que requieran reposición.

3. Los administradores de minimarkets valoran recibir alertas cuando las condiciones de almacenamiento puedan afectar determinados productos.

4. Los administradores de minimarkets necesitan consultar la disponibilidad de productos ofrecidos por proveedores conectados.

5. Los proveedores necesitan visualizar y gestionar sus productos, disponibilidad y lotes desde un único sistema.

6. Los proveedores requieren recibir pedidos estructurados de los minimarkets, responderlos, generar órdenes de envío y consultar el estado de sus operaciones.

7. Ambos segmentos necesitan consultar el estado de un pedido y mantener información actualizada sobre el proceso de abastecimiento.

**User Outcome Assumptions**

1. Los administradores de minimarkets tendrán mayor confianza en la información de su inventario al disponer de un registro centralizado de productos, stock, lotes y vencimientos.

2. Los administradores de minimarkets podrán identificar oportunamente productos con niveles de stock bajos y necesidades de reposición.

3. Los administradores de minimarkets podrán identificar condiciones ambientales anómalas que puedan representar un riesgo para los productos almacenados.

4. Los administradores de minimarkets podrán revisar las órdenes de envío generadas por los proveedores y decidir si aceptarlas o rechazarlas antes de modificar su inventario.

5. Los proveedores podrán consultar sus productos y disponibilidad, responder pedidos, generar órdenes de envío y realizar seguimiento de su estado.

6. Los usuarios experimentarán una reducción de la incertidumbre respecto al estado de los pedidos de abastecimiento.

7. Los usuarios de ambos segmentos podrán tomar decisiones operativas con mayor rapidez al contar con información centralizada y actualizada.

8. Los visitantes de la Landing Page podrán comprender rápidamente la propuesta de valor de MarketGo para su segmento y decidir si registrarse.

Los resultados de usuario se comprobarán con tareas de consulta de inventario y vencimientos, detección de alertas, identificación de stock bajo, creación y revisión de pedidos, y consulta de su estado. Se observarán el tiempo de ejecución, la finalización de la tarea y los errores; las entrevistas y pruebas permitirán contrastar estos resultados con las prácticas actuales de cada segmento.

**Feature Assumptions**

Cada Feature Assumption (FA) da origen a un Hypothesis Statement, de modo que existe una relación 1 a 1 entre ambas listas.

1. Se considera que permitir registrar, consultar, buscar, filtrar y actualizar productos, cantidades, lotes y vencimientos, priorizando la salida de los lotes más próximos a vencer (criterio FEFO), facilitará el control centralizado del inventario del minimarket.

2. Se plantea que las alertas configurables sobre productos próximos a vencer y condiciones inadecuadas de temperatura o humedad permitirán identificar oportunamente productos en riesgo.

3. Se considera que visualizar registros de temperatura y humedad permitirá al administrador supervisar las condiciones de conservación de los productos.

4. Se plantea que permitir a los proveedores mantener actualizados sus productos, lotes y disponibilidad facilitará que los minimarkets consulten alternativas de abastecimiento desde la plataforma.

5. Se considera que permitir al administrador crear pedidos dirigidos a un proveedor, y al proveedor aceptarlos o rechazarlos y generar la orden de envío correspondiente, permitirá centralizar la coordinación del abastecimiento.

6. Se plantea que reservar al administrador la decisión de aceptar o rechazar las órdenes de envío, actualizando el inventario automáticamente solo cuando se acepten, permitirá mantener el control y la trazabilidad de las entradas de productos.

7. Se considera que ofrecer dashboards diferenciados, indicadores, alertas e historial de operaciones permitirá a cada segmento consultar rápidamente el estado de sus actividades y tomar decisiones con información centralizada.

8. Se plantea que un sistema de autenticación, roles y permisos permitirá que administradores y proveedores accedan únicamente a las funcionalidades y datos correspondientes a su negocio.

9. Se considera que una Landing Page con llamadas a la acción diferenciadas para minimarkets y proveedores, video del producto, planes y formulario de contacto convertirá a los visitantes en usuarios registrados.

---

#### 1.2.2.3. Lean UX Hypothesis Statements.

Las hipótesis se redactaron con la plantilla oficial *"We believe we will achieve [business outcome] if [personas] attain [user outcome] with [feature]"*. Se formuló una hipótesis por cada Feature Assumption, y las columnas BO, UO y FA indican el número del Business Outcome, User Outcome y Feature Assumption enumerados en la sección anterior.

| # | Hypothesis Statement | BO | UO | FA |
|---|---|:---:|:---:|:---:|
| H1 | *We believe we will achieve* greater traceability of products, batches and expiration dates *if* minimarket administrators like Russell Estrada *attain* higher confidence in their inventory information *with* a centralized inventory module to register, search, filter and update products, batches and expirations. | 2 | 1 | 1 |
| H2 | *We believe we will achieve* fewer products written off due to expiration or spoilage *if* minimarket administrators like Russell Estrada *attain* timely detection of near-expiry products and risky storage conditions *with* configurable expiration and storage condition alerts. | 1 | 3 | 2 |
| H3 | *We believe we will achieve* a reduction in the time required to identify products or batches at risk *if* minimarket administrators like Russell Estrada *attain* continuous visibility of the conditions in which their products are stored *with* temperature and humidity records for each storage area. | 3 | 3 | 3 |
| H4 | *We believe we will achieve* better information for replenishment decisions *if* suppliers like Marco Antonio Ríos *attain* a single, up-to-date view of their products, batches and availability that minimarkets can consult *with* a supplier product catalog. | 5 | 5 | 4 |
| H5 | *We believe we will achieve* increased traceability of orders from their creation to their shipment *if* suppliers like Marco Antonio Ríos *attain* less uncertainty about the orders they must fulfill, without transcribing WhatsApp messages *with* a structured workflow in which administrators create orders and suppliers accept them and generate shipping orders. | 6 | 6 | 5 |
| H6 | *We believe we will achieve* complete traceability of product entries into the inventory *if* minimarket administrators like Russell Estrada *attain* the ability to review shipping orders and accept or reject them before their inventory is modified *with* shipping order reception that automatically updates the inventory only when accepted. | 6 | 4 | 6 |
| H7 | *We believe we will achieve* a better capacity to anticipate replenishment needs *if* minimarket administrators like Russell Estrada and suppliers like Marco Antonio Ríos *attain* faster operational decisions and early identification of low-stock products *with* role-based dashboards with indicators, alerts and an operations history. | 4 | 2 | 7 |
| H8 | *We believe we will achieve* trustworthy order and inventory traceability across both segments *if* minimarket administrators like Russell Estrada and suppliers like Marco Antonio Ríos *attain* the confidence that each party can only see and modify the data of its own business *with* authentication, roles and permissions per segment. | 6 | 7 | 8 |
| H9 | *We believe we will achieve* a growing base of registered minimarkets and suppliers *if* visitors of the Landing Page *attain* a quick understanding of how MarketGo solves the problems of their segment *with* a responsive Landing Page with segment-specific calls to action, product video, plans and a contact form. | 7 | 8 | 9 |

Estas hipótesis se validarán mediante pruebas con usuarios sobre el prototipo y, posteriormente, con métricas de uso de la plataforma, comparándolas con la línea base de las herramientas actuales de cada segmento (tiempo de ejecución, finalización de la tarea y errores).

---

#### 1.2.2.4. Lean UX Canvas.
El Canvas sintetiza la propuesta de valor de MarketGo a partir de los User Personas de la sección 2.3.1, **Russell Estrada** (administrador de minimarket orgánico) y **Marco Antonio Ríos** (coordinador comercial de una distribuidora orgánica B2B), y de los competidores analizados en la sección 2.1.


<table>
  <tr>
    <td valign="top" width="33%">
      <strong>1. Business problem</strong>
      <br><br>
      Los minimarkets de productos orgánicos en Lima controlan inventario, lotes, vencimientos y conservación con revisiones físicas, libretas y hojas de cálculo, y coordinan su abastecimiento por WhatsApp (100% de los administradores entrevistados).
      <br><br>
      Esto provoca mermas por vencimiento o pérdida de cadena de frío, errores de stock al transcribir pedidos y llamadas constantes para confirmar despachos.
      <br><br>
      FreshTracker, ShelfLife y Peru Marketplace resuelven solo una parte (conservación, inventario o conexión B2B) y ninguna conecta el abastecimiento con el inventario y la conservación.
    </td>
    <td rowspan="2" valign="top" width="34%">
      <strong>5. Solution ideas</strong>
      <br><br>
      - Inventario centralizado con lotes y vencimientos (FA1).
      <br><br>
      - Alertas de vencimiento y de condiciones de conservación (FA2).
      <br><br>
      - Registros de temperatura y humedad con datos inicialmente simulados (FA3).
      <br><br>
      - Catálogo del proveedor con disponibilidad real (FA4).
      <br><br>
      - Pedido creado por el administrador → aceptado por el proveedor → orden de envío (FA5).
      <br><br>
      - Recepción de la orden de envío que actualiza automáticamente el inventario (FA6).
      <br><br>
      - Dashboards por rol con indicadores, alertas e historial (FA7).
      <br><br>
      - Autenticación, roles y permisos por segmento (FA8).
    </td>
    <td valign="top" width="33%">
      <strong>2. Business outcomes</strong>
      <br><br>
      - Reducir en 30% las bajas por vencimiento o deterioro de los minimarkets suscritos en 6 meses.
      <br><br>
      - Reducir de 24 h a menos de 4 h el tiempo entre la creación de un pedido y su orden de envío en el 80% de los pedidos.
      <br><br>
      - Lograr que el 100% de las órdenes de envío aceptadas actualicen el inventario sin registro manual.
      <br><br>
      - Alcanzar 20 minimarkets y 5 proveedores activos al cierre del primer semestre.
    </td>
  </tr>
  <tr>
    <td valign="top">
      <strong>3. Users &amp; customers</strong>
      <br><br>
      - <strong>Russell Estrada</strong> (28 años, Lima): administrador de minimarket orgánico, opera desde el celular, usa Excel y WhatsApp y tiene baja adopción de nuevas herramientas.
      <br><br>
      - <strong>Marco Antonio Ríos</strong> (32 años, Lurín): coordinador comercial de una distribuidora que atiende 30 minimarkets con un catálogo de 120 productos.
    </td>
    <td valign="top">
      <strong>4. User outcomes &amp; benefits</strong>
      <br><br>
      - Russell: dejar de perder dinero por mermas al enterarse a tiempo de vencimientos y fallas de refrigeración, sin revisar físicamente el almacén.
      <br><br>
      - Russell: mantener el stock real al aceptar una orden de envío, sin transcribir datos de WhatsApp a Excel.
      <br><br>
      - Marco: recibir pedidos estructurados y despachar sin errores de transcripción.
      <br><br>
      - Marco: dejar de atender llamadas de confirmación, porque el minimarket ve el estado de su pedido.
      <br><br>
      - Ambos: una herramienta sencilla, usable desde el celular y con una curva de aprendizaje corta.
    </td>
  </tr>
  <tr>
    <td valign="top">
      <strong>6. Hypotheses</strong>
      <br><br>
      - H1: más trazabilidad si Russell confía en su inventario gracias al módulo de inventario y lotes.
      <br><br>
      - H2 y H3: menos mermas si Russell detecta a tiempo vencimientos y condiciones riesgosas gracias a alertas y registros de conservación.
      <br><br>
      - H4: mejores decisiones de reposición si Marco mantiene un catálogo con disponibilidad real.
      <br><br>
      - H5 y H6: pedidos trazables de inicio a fin si Marco despacha con órdenes de envío y Russell las acepta antes de actualizar su inventario.
      <br><br>
      - H7 y H8: reposición anticipada y datos confiables gracias a dashboards por rol con permisos.
    </td>
    <td valign="top">
      <strong>7. What's the most important thing we need to learn first?</strong>
      <br><br>
      - Si Russell confía en las alertas y en la actualización automática del inventario lo suficiente como para abandonar su control en Excel.
      <br><br>
      - Si Marco está dispuesto a recibir y responder pedidos en MarketGo en lugar de WhatsApp.
      <br><br>
      - Si la separación de funciones (el administrador crea el pedido y acepta la recepción; el proveedor responde y despacha) es clara para ambos segmentos.
    </td>
    <td valign="top">
      <strong>8. What's the least amount of work we need to do to learn the next most important thing?</strong>
      <br><br>
      - Crear un prototipo navegable con datos ficticios realistas de inventario, lotes, vencimientos, temperatura, humedad y alertas.
      <br><br>
      - Probar con 3 administradores y 3 proveedores el flujo completo: crear pedido → aceptarlo → generar orden de envío → aceptar la recepción y ver el inventario actualizado.
      <br><br>
      - Medir finalización de tareas, tiempo, errores y comprensión frente a su proceso actual con WhatsApp y Excel, y cerrar con una breve entrevista sobre confianza e intención de adopción.
    </td>
  </tr>
</table>


**Diferenciación frente a la competencia**

| Capacidad | MarketGo | FreshTracker | ShelfLife | Peru Marketplace |
|---|:---:|:---:|:---:|:---:|
| Inventario, lotes y vencimientos | ✔ | ✘ | ✔ | ✘ |
| Monitoreo de temperatura y humedad con alertas | ✔ | ✔ | ✘ | ✘ |
| Pedidos y órdenes de envío entre minimarket y proveedor | ✔ | ✘ | ✘ | ✔ |
| Recepción que actualiza automáticamente el inventario | ✔ | ✘ | ✘ | ✘ |
| Dashboards con permisos por rol (minimarket / proveedor) | ✔ | ✘ | ✘ | ✘ |
| Enfoque especializado en productos orgánicos | ✔ | ✘ | ✘ | ✘ |

La propuesta de valor diferencial de MarketGo es **conectar el abastecimiento con el inventario y la conservación**: un pedido aceptado por el proveedor se convierte en una orden de envío que, al ser aceptada por el minimarket, actualiza su inventario y sus lotes, los cuales quedan inmediatamente bajo control de vencimientos y alertas de conservación.

---

---

## 1.3. Segmentos objetivo.

La solución está dirigida a **dos segmentos objetivos principales** que participan directamente en la cadena de abastecimiento de productos orgánicos: **administradores de minimarkets y proveedores**.

Estos segmentos representan dos tipos de organizaciones con necesidades de negocio diferentes. Por ello, la plataforma utiliza un **dashboard común**, pero aplica permisos específicos para cada segmento. Los administradores de minimarkets cuentan con permisos de lectura y escritura sobre la información de su operación, mientras que los proveedores cuentan con permisos de consulta y acciones específicas para generar pedidos, sin acceso para modificar directamente el inventario del minimarket.

Los roles operativos que puedan existir dentro de cada empresa forman parte de la estructura interna de cada segmento y no constituyen segmentos objetivos independientes.

### 1.3.1. Segmento objetivo 1: Administradores de Minimarkets

| Dimensión | Detalle del perfil |
|---|---|
| **Perfil Demográfico** | Propietarios, administradores o responsables de pequeños y medianos minimarkets dedicados a la comercialización de productos orgánicos y alimentos frescos. Son responsables de supervisar las operaciones comerciales y tomar decisiones relacionadas con inventario, conservación y abastecimiento. |
| **Perfil Geográfico** | Negocios ubicados principalmente en zonas urbanas con demanda de productos orgánicos y necesidad de mantener un abastecimiento constante. El segmento inicial puede concentrarse en Lima Metropolitana. |
| **Perfil Psicográfico** | Personas orientadas a mantener la calidad de sus productos, reducir pérdidas y asegurar la disponibilidad constante de mercadería. Valoran soluciones sencillas que permitan controlar las operaciones del negocio y tomar decisiones basadas en información actualizada. |
| **Puntos de Dolor** | Pérdidas ocasionadas por deterioro o vencimiento de productos, dificultad para controlar lotes y fechas de vencimiento, falta de visibilidad sobre las condiciones de almacenamiento, desabastecimiento y dificultad para coordinar pedidos con proveedores. |
| **Uso de Tecnología** | Utilizan herramientas digitales para administrar ventas, inventarios y comunicación con proveedores, aunque pueden depender de hojas de cálculo, aplicaciones de mensajería y sistemas independientes que no integran toda la información operativa. |

### 1.3.2. Segmento objetivo 2: Proveedores

| Dimensión | Detalle del perfil |
|---|---|
| **Perfil Demográfico** | Empresas, productores, distribuidores o comerciantes mayoristas de productos orgánicos que abastecen a minimarkets. Sus representantes participan en la oferta de productos y en las operaciones de abastecimiento realizadas mediante la plataforma. |
| **Perfil Geográfico** | Proveedores ubicados en zonas productoras, centros de distribución o áreas comerciales que atienden a minimarkets y otros negocios comercializadores de productos orgánicos. |
| **Perfil Psicográfico** | Negocios orientados a mantener una relación comercial eficiente con sus clientes y facilitar el abastecimiento oportuno de productos. Valoran la trazabilidad, organización y visibilidad de las operaciones relacionadas con los productos que ofrecen. |
| **Puntos de Dolor** | Dificultad para mantener visibilidad sobre los pedidos realizados, falta de centralización de la información de las operaciones comerciales y dependencia de diferentes canales de comunicación para coordinar el abastecimiento. |
| **Uso de Tecnología** | Utilizan herramientas digitales, hojas de cálculo y aplicaciones de comunicación para gestionar sus operaciones comerciales, pero pueden carecer de una plataforma especializada que centralice la información de los productos ofrecidos y los pedidos realizados por los minimarkets. |

