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

Nuestra solución MarketGo, es una plataforma web para la gestión de inventarios, abastecimiento y monitoreo de productos orgánicos, que conecta a administradores de minimarkets y proveedores mediante un ecosistema digital centralizado.

Para los administradores de minimarkets, permite gestionar productos, inventario, lotes, vencimientos, ubicaciones, mermas y donaciones, además de monitorear temperatura y humedad para detectar posibles riesgos de conservación.

Para los proveedores, permite gestionar productos, disponibilidad y lotes, así como crear y consultar pedidos de abastecimiento dirigidos a los minimarkets. Los proveedores no pueden modificar directamente el inventario.

Los pedidos generados por los proveedores son revisados por el administrador, quien puede aceptarlos o rechazarlos. Si el pedido es aceptado, se registra la operación y se actualiza el inventario; si es rechazado, el inventario permanece sin cambios.

La plataforma integra inventario, abastecimiento, trazabilidad y monitoreo IoT. Durante la implementación, los datos de los sensores podrán ser simulados para validar los flujos de monitoreo y alertas sin depender de dispositivos físicos.

De esta manera, MarketGo busca mejorar la gestión y abastecimiento de productos orgánicos mediante información centralizada y permisos diferenciados, bajo el principio de que **el proveedor puede iniciar una operación de abastecimiento, pero solamente el administrador del minimarket puede modificar su inventario**.

**Propuesta de valor por segmento:** Para el administrador de minimarket, MarketGo propone reunir el control de stock, lotes, vencimientos y condiciones de conservación con la decisión sobre los pedidos del proveedor, de modo que pueda detectar productos en riesgo y reponer sin perder el control de su inventario. Para el proveedor, propone mantener su catálogo y disponibilidad y seguir el estado de los pedidos dirigidos a los minimarkets en el mismo flujo. Frente a las soluciones comerciales revisadas, el diferencial propuesto es la combinación de trazabilidad de perecibles, alertas de conservación y coordinación entre ambos segmentos con permisos diferenciados.

### 1.2.1 Antecedentes y problemática

El sistema alimentario peruano enfrenta importantes pérdidas de productos a lo largo de su cadena de suministro. Se estima que en el Perú se pierden aproximadamente 12,8 millones de toneladas de alimentos al año, equivalente al 47,6% de la oferta anual de alimentos. Dentro de estas pérdidas, una proporción importante corresponde a frutas y hortalizas, productos particularmente sensibles a factores como la temperatura, humedad, manipulación y tiempo de almacenamiento (OECD, 2025; Bedoya-Perales & Dal’ Magro, 2021). Esta situación evidencia la necesidad de mejorar los mecanismos de gestión y conservación de productos perecibles.

En los minimarkets, esta problemática se relaciona con las dificultades para mantener un control adecuado sobre el inventario, lotes, fechas de vencimiento y condiciones de almacenamiento. La utilización de registros manuales, hojas de cálculo y herramientas independientes puede dificultar la identificación oportuna de productos próximos a vencer, niveles bajos de stock o condiciones ambientales inadecuadas, incrementando el riesgo de deterioro, desperdicio y desabastecimiento. Además, estudios aplicados a tiendas de conveniencia en Lima evidencian que la optimización del inventario puede mejorar indicadores operativos como la reposición, el nivel de servicio, la reducción de quiebres de stock y la rentabilidad del negocio (Zavaleta-Zarate et al., 2026).

Asimismo, el abastecimiento requiere una coordinación constante entre los administradores de minimarkets y los proveedores. Mientras los administradores necesitan gestionar sus necesidades de reposición, los proveedores requieren controlar la disponibilidad de sus productos y generar pedidos dirigidos a los establecimientos. La ausencia de un flujo centralizado puede generar errores, retrasos y poca trazabilidad de las operaciones. En este contexto, **MarketGo** propone una plataforma especializada que integra la gestión de inventarios, lotes, vencimientos, abastecimiento y monitoreo de condiciones de almacenamiento, permitiendo que los proveedores generen pedidos y que los administradores mantengan el control sobre su aceptación y actualización del inventario.

**Objetivos de la solución:**

- Centralizar la gestión de productos, inventario, lotes, vencimientos y condiciones de almacenamiento de productos orgánicos.
- Facilitar la coordinación de abastecimiento entre administradores de minimarkets y proveedores mediante un flujo de pedidos controlado.
- Anticipar riesgos operativos asociados a stock bajo, vencimientos próximos y condiciones ambientales inadecuadas.
- Mejorar la trazabilidad de las operaciones de inventario y abastecimiento.

**Técnica "The 5W's y 2H's" aplicada al problema:**

| The 5W's y 2H's | Pregunta | Descripción |
|:---|:---|:---|
| **Who** | ¿Quiénes están involucrados? | Administradores de minimarkets responsables de gestionar inventarios, conservación y abastecimiento, y proveedores encargados de gestionar la disponibilidad de productos y generar pedidos de abastecimiento. |
| **What** | ¿Cuál es el problema? | Dificultad para gestionar de manera integrada inventarios, niveles de stock, lotes, vencimientos, condiciones de almacenamiento y operaciones de abastecimiento de productos orgánicos. |
| **Where** | ¿Dónde ocurre? | En los procesos de almacenamiento, gestión de inventarios y abastecimiento de productos orgánicos en minimarkets, así como en la gestión de productos, disponibilidad y pedidos de los proveedores. |
| **When** | ¿Cuándo sucede? | Durante el almacenamiento, control de inventarios, seguimiento de lotes y vencimientos, identificación de necesidades de reposición, generación de pedidos y aceptación o rechazo de las operaciones de abastecimiento. |
| **Why** | ¿Por qué sucede? | Debido a la fragmentación de la información, el uso de procesos manuales y la ausencia de una plataforma especializada que integre inventario, abastecimiento y monitoreo de las condiciones de almacenamiento. |
| **How** | ¿Cómo se manifiesta? | Mediante dificultades para identificar productos con stock bajo, controlar lotes y vencimientos, detectar condiciones ambientales anómalas, consultar disponibilidad, generar pedidos y realizar seguimiento de las operaciones de abastecimiento. |
| **How Much** | ¿Cuánto impacto tiene? | En el Perú se pierden aproximadamente **12,8 millones de toneladas de alimentos al año**, equivalentes al **47,6% de la oferta anual de alimentos**. Además, alrededor del **44% de estas pérdidas corresponde a frutas y hortalizas**, productos especialmente sensibles a las condiciones de almacenamiento (OECD, 2025; Bedoya-Perales & Dal’ Magro, 2021). A nivel operativo, estas pérdidas pueden traducirse en productos deteriorados o vencidos, desabastecimiento y mayores costos de gestión. |

---

### 1.2.2 Lean UX Process.

#### 1.2.2.1. Lean UX Problem Statements.

En el mercado peruano, los administradores de minimarkets que comercializan productos orgánicos necesitan controlar inventarios, lotes, vencimientos y condiciones de almacenamiento para evitar mermas y reponer a tiempo. Las entrevistas muestran casos de uso combinado de POS, hojas de cálculo, libretas y mensajería; esa dispersión dificulta detectar productos en riesgo y conocer el stock disponible. Los proveedores, por su parte, necesitan mantener actualizados su catálogo, lotes y disponibilidad, y dar seguimiento a los pedidos dirigidos a los minimarkets. La coordinación mediante archivos y conversaciones separadas dificulta confirmar cantidades, cambios y estados de pedido. La magnitud de las pérdidas alimentarias en el Perú y los hallazgos de las entrevistas contextualizan el problema, sin representar una medición de merma específica de los minimarkets entrevistados.

Existen soluciones de gestión comercial e inventario para minimarkets, revisadas en el análisis competitivo. La oportunidad de 5bits es atender de forma integrada la conservación de productos orgánicos, la trazabilidad por lotes y la coordinación de pedidos entre ambos segmentos. Para el administrador, el problema es no identificar a tiempo vencimientos, condiciones de almacenamiento riesgosas y necesidades de reposición, y no mantener un control verificable sobre la entrada de productos a su inventario. Para el proveedor, es no contar con una vista compartida y actualizada de disponibilidad y estado de pedidos. MarketGo busca reducir estas dificultades mediante un flujo en el que el proveedor genera el pedido y el administrador lo acepta o rechaza antes de actualizar el inventario.

**Problem Statement:** ¿Cómo podemos ayudar a administradores de minimarkets de productos orgánicos y a sus proveedores a identificar riesgos de pérdida y necesidades de reposición, y a coordinar pedidos con trazabilidad y control de inventario, mediante una plataforma integrada de productos, lotes, vencimientos y condiciones de almacenamiento? En esta etapa se validarán el diseño y los flujos con datos de monitoreo simulados; el uso de sensores físicos queda fuera del alcance inicial.

1. **Domain:** Gestión logística, abastecimiento y monitoreo de productos orgánicos.

2. **Customer Segments:** Administradores de minimarkets y proveedores de productos orgánicos.

3. **Pain Points:** Pérdidas por deterioro o vencimiento, falta de visibilidad sobre las condiciones de almacenamiento, dificultades para controlar niveles de stock, lotes y vencimientos, problemas para consultar disponibilidad de productos y coordinar pedidos de abastecimiento.

4. **Gap:** Las soluciones comerciales comparadas cubren componentes de inventario y compras; la oportunidad identificada es integrar la conservación de productos orgánicos, la trazabilidad por lotes y el flujo de pedidos entre minimarket y proveedor, con permisos diferenciados para modificar el inventario.

5. **Vision/Strategy:** Centralizar la información operativa para identificar riesgos, anticipar necesidades de reposición, gestionar inventarios y facilitar el abastecimiento mediante un flujo en el que los proveedores generen pedidos y los administradores puedan aceptarlos o rechazarlos antes de actualizar el inventario.

6. **Initial Segment:** Administradores de minimarkets y proveedores de productos orgánicos que requieran mejorar el control de inventarios, conservación y abastecimiento.

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

6. Incrementar la trazabilidad de los pedidos desde su creación por parte del proveedor hasta su aceptación o rechazo por parte del administrador.

Estos resultados se evaluarán, respectivamente, mediante la cantidad de productos dados de baja por vencimiento o deterioro; el porcentaje de productos con lote y vencimiento registrados; el tiempo para identificar productos en riesgo; el tiempo entre la detección de stock bajo y la decisión de reposición; la disponibilidad de información vigente sobre productos y pedidos; y el porcentaje de pedidos con estado e historial de decisiones consultables. Se compararán con una línea base levantada durante las pruebas con usuarios.

**User Assumptions**

1. Los administradores de minimarkets necesitan visualizar rápidamente el estado de su inventario y los productos próximos a vencer.

2. Los administradores de minimarkets necesitan identificar productos con niveles de stock que requieran reposición.

3. Los administradores de minimarkets valoran recibir alertas cuando las condiciones de almacenamiento puedan afectar determinados productos.

4. Los administradores de minimarkets necesitan consultar la disponibilidad de productos ofrecidos por proveedores conectados.

5. Los proveedores necesitan visualizar y gestionar sus productos, disponibilidad y lotes desde un único sistema.

6. Los proveedores requieren generar pedidos de abastecimiento dirigidos a los minimarkets y consultar el estado de sus operaciones.

7. Ambos segmentos necesitan consultar el estado de un pedido y mantener información actualizada sobre el proceso de abastecimiento.

**User Outcome Assumptions**

1. Los administradores de minimarkets tendrán mayor confianza en la información de su inventario al disponer de un registro centralizado de productos, stock, lotes y vencimientos.

2. Los administradores de minimarkets podrán identificar oportunamente productos con niveles de stock bajos y necesidades de reposición.

3. Los administradores de minimarkets podrán identificar condiciones ambientales anómalas que puedan representar un riesgo para los productos almacenados.

4. Los administradores de minimarkets podrán revisar los pedidos generados por proveedores y decidir si aceptarlos o rechazarlos antes de modificar su inventario.

5. Los proveedores podrán consultar sus productos y disponibilidad, generar pedidos de abastecimiento y realizar seguimiento de su estado.

6. Los usuarios experimentarán una reducción de la incertidumbre respecto al estado de los pedidos de abastecimiento.

7. Los administradores de ambos segmentos podrán tomar decisiones operativas con mayor rapidez al contar con información centralizada y actualizada.

Los resultados de usuario se comprobarán con tareas de consulta de inventario y vencimientos, detección de alertas, identificación de stock bajo, creación y revisión de pedidos, y consulta de su estado. Se observarán el tiempo de ejecución, la finalización de la tarea y los errores; las entrevistas y pruebas permitirán contrastar estos resultados con las prácticas actuales de cada segmento.

**Feature Assumptions**

1. Se considera que permitir registrar, consultar, buscar, filtrar y actualizar productos, cantidades, lotes y vencimientos facilitará el control centralizado del inventario del minimarket.

2. Se plantea que las alertas configurables sobre productos próximos a vencer y condiciones inadecuadas de temperatura o humedad permitirán identificar oportunamente productos en riesgo.

3. Se considera que visualizar registros de temperatura y humedad permitirá al administrador supervisar las condiciones de conservación de los productos.

4. Se plantea que permitir a los proveedores mantener actualizados sus productos, lotes y disponibilidad facilitará que los minimarkets consulten alternativas de abastecimiento desde la plataforma.

5. Se considera que permitir al administrador comunicar necesidades de reposición y al proveedor generar pedidos dirigidos al minimarket permitirá centralizar la coordinación del abastecimiento.

6. Se plantea que reservar al administrador la decisión de aceptar o rechazar pedidos, actualizando el inventario únicamente cuando se acepten, permitirá mantener el control y la trazabilidad de las entradas de productos.

7. Se considera que ofrecer dashboards diferenciados, indicadores, alertas e historial de operaciones permitirá a cada segmento consultar rápidamente el estado de sus actividades y tomar decisiones con información centralizada.

8. Se plantea que un sistema de autenticación, roles y permisos permitirá que administradores y proveedores accedan únicamente a las funcionalidades y datos correspondientes a su negocio.

---

#### 1.2.2.3. Lean UX Hypothesis Statements.

Cada hipótesis sigue el esquema resultado de negocio, usuarios, resultado de usuario y funcionalidad. Las referencias entre paréntesis remiten a los supuestos de negocio, de resultado de negocio, de usuario y de resultado de usuario enumerados arriba.

**Hypothesis 1** Creemos que mejoraremos la trazabilidad y reduciremos el tiempo para identificar productos en riesgo si los administradores de minimarkets pueden consultar stock, lotes y vencimientos en un registro centralizado mediante el módulo de inventario y su dashboard. Lo comprobaremos al comparar el porcentaje de productos con lote y vencimiento registrados y el tiempo de identificación de un producto crítico frente al proceso actual.

**Hypothesis 2** Creemos que reduciremos las bajas por deterioro y el tiempo de detección de condiciones riesgosas si los administradores identifican a tiempo productos o lotes afectados mediante alertas de temperatura y humedad. Primero comprobaremos la detección y atención de alertas con datos simulados; la reducción de bajas y la integración con sensores reales requerirán validación posterior en operación.

**Hypothesis 3** Creemos que mejoraremos la reposición y la información disponible para decidir compras si los administradores pueden identificar stock bajo y consultar disponibilidad de proveedores mediante alertas de inventario y catálogo compartido. Lo comprobaremos con el tiempo entre la detección de stock bajo y la decisión de reposición, y con tareas de consulta de disponibilidad completadas.

**Hypothesis 4** Creemos que incrementaremos la trazabilidad de los pedidos y reduciremos la dispersión de información si los proveedores pueden mantener disponibles sus productos y lotes, crear pedidos dirigidos a minimarkets y consultar su estado mediante el catálogo y el módulo de pedidos. Lo comprobaremos con el porcentaje de pedidos que conserva estado e historial consultables y con tareas de creación y seguimiento completadas sin recurrir a otros canales.

**Hypothesis 5** Creemos que mejoraremos el control del inventario y la trazabilidad del abastecimiento si los administradores pueden revisar, aceptar o rechazar pedidos mediante un flujo de aprobación con historial. Lo comprobaremos verificando que cada decisión quede registrada, que solo los pedidos aceptados actualicen el inventario y que los usuarios puedan consultar el estado resultante.

**Hypothesis 6** Creemos que reduciremos el tiempo de consulta operativa y facilitaremos la adopción si administradores y proveedores pueden realizar sus tareas principales desde dashboards diferenciados con una interfaz sencilla. Lo comprobaremos con tareas de ambos segmentos, observando tiempo, finalización, errores y dificultades de uso frente a sus herramientas actuales.

**Hypothesis 7** Creemos que un servicio SaaS será viable para minimarkets y proveedores si estos perciben que la reducción de mermas y la mejora del abastecimiento compensan el costo, mediante el acceso a los módulos centrales de MarketGo sin infraestructura propia. Lo comprobaremos con entrevistas sobre disposición de adopción y pago, contrastadas posteriormente con costos y resultados medidos en pilotos.

---

#### 1.2.2.4. Lean UX Canvas.

El Canvas sintetiza la propuesta de valor descrita  para las dos segmentos.

<table>
  <tr>
    <td valign="top">
      <strong>Business problem</strong>
      <br><br>
      El administrador de minimarket consulta existencias, lotes y conservación en herramientas dispersas mientras necesita detectar riesgos y decidir una reposición sin perder el control del inventario.
      <br><br>
      El proveedor mantiene su oferta y coordina pedidos por canales separados, lo que dificulta confirmar disponibilidad, cantidades y estado de cada operación.
      <br><br>
      El análisis competitivo muestra herramientas de inventario y compras; la oportunidad por comprobar es integrar conservación de perecibles, trazabilidad por lotes y pedidos entre ambos segmentos con aprobación del administrador.
    </td>
    <td rowspan="2" valign="top">
      <strong>Solution ideas</strong>
      <br><br>
      - Registro de stock, lotes y vencimientos para el administrador (H1)
      <br><br>
      - Alertas de conservación con datos inicialmente simulados (H2)
      <br><br>
      - Alertas de stock bajo y consulta de disponibilidad del proveedor (H3)
      <br><br>
      - Catálogo del proveedor y creación y seguimiento de pedidos (H4)
      <br><br>
      - Aceptación o rechazo por el administrador antes de actualizar inventario (H5)
      <br><br>
      - Dashboards diferenciados por segmento (H6)
      <br><br>
      - Acceso SaaS a los módulos centrales, sujeto a validación de adopción y costo (H7)
    </td>
    <td valign="top">
      <strong>Business Outcomes</strong>
      <br><br>
      - Bajas por deterioro o vencimiento: comparar su cantidad con una línea base operativa futura
      <br><br>
      - Trazabilidad de productos: medir el porcentaje con lote y vencimiento registrados
      <br><br>
      - Reposición: medir el tiempo entre detección de stock bajo y decisión
      <br><br>
      - Pedidos: medir el porcentaje con estado e historial de decisiones consultables
      <br><br>
    </td>
  </tr>
  <tr>
    <td valign="top">
      <strong>Users and customers</strong>
      <br><br>
      - Administrador de minimarket: Persona que deciden sobre inventario, conservación y reposición.
      <br>
      - Proveedor de productos orgánicos: Persona que mantiene oferta y coordina pedidos.
    </td>
    <td valign="top">
      <strong>User benefits</strong>
      <br><br>
      - Administrador: localizar existencias, lotes, vencimientos y condiciones de riesgo al revisar productos y conservación.
      <br><br>
      - Administrador: decidir reposición y aceptar o rechazar un pedido antes de registrar la entrada al inventario.
      <br><br>
      - Proveedor: actualizar oferta y disponibilidad y comprobar el estado de cada pedido dirigido al minimarket.
      <br><br>
      - Ambos: reducir incertidumbre al consultar un historial compartido de la operación.
    </td>
  </tr>
  <tr>
    <td valign="top">
      <strong>Hypotheses</strong>
      <br><br>
      - H1:  Creemos que mejoraremos la trazabilidad y reduciremos el tiempo para identificar productos en riesgo si los administradores de minimarkets pueden consultar stock, lotes y vencimientos en un registro centralizado mediante el módulo de inventario y su dashboard. Lo comprobaremos al comparar el porcentaje de productos con lote y vencimiento registrados y el tiempo de identificación de un producto crítico frente al proceso actual.
      <br><br>
      - H2: Creemos que reduciremos las bajas por deterioro y el tiempo de detección de condiciones riesgosas si los administradores identifican a tiempo productos o lotes afectados mediante alertas de temperatura y humedad. Primero comprobaremos la detección y atención de alertas con datos simulados; la reducción de bajas y la integración con sensores reales requerirán validación posterior en operación.
      <br><br>
      - H3: Creemos que mejoraremos la reposición y la información disponible para decidir compras si los administradores pueden identificar stock bajo y consultar disponibilidad de proveedores mediante alertas de inventario y catálogo compartido. Lo comprobaremos con el tiempo entre la detección de stock bajo y la decisión de reposición, y con tareas de consulta de disponibilidad completadas.
      <br><br>
      - H4: Creemos que incrementaremos la trazabilidad de los pedidos y reduciremos la dispersión de información si los proveedores pueden mantener disponibles sus productos y lotes, crear pedidos dirigidos a minimarkets y consultar su estado mediante el catálogo y el módulo de pedidos. Lo comprobaremos con el porcentaje de pedidos que conserva estado e historial consultables y con tareas de creación y seguimiento completadas sin recurrir a otros canales.
      <br><br>
      - H5: Creemos que mejoraremos el control del inventario y la trazabilidad del abastecimiento si los administradores pueden revisar, aceptar o rechazar pedidos mediante un flujo de aprobación con historial. Lo comprobaremos verificando que cada decisión quede registrada, que solo los pedidos aceptados actualicen el inventario y que los usuarios puedan consultar el estado resultante.
      <br><br>
      - H6: Creemos que reduciremos el tiempo de consulta operativa y facilitaremos la adopción si administradores y proveedores pueden realizar sus tareas principales desde dashboards diferenciados con una interfaz sencilla. Lo comprobaremos con tareas de ambos segmentos, observando tiempo, finalización, errores y dificultades de uso frente a sus herramientas actuales.
      <br><br>
      - H7: Creemos que un servicio SaaS será viable para minimarkets y proveedores si estos perciben que la reducción de mermas y la mejora del abastecimiento compensan el costo, mediante el acceso a los módulos centrales de MarketGo sin infraestructura propia. Lo comprobaremos con entrevistas sobre disposición de adopción y pago, contrastadas posteriormente con costos y resultados medidos en pilotos.
    </td>
    <td valign="top">
      <strong>What’s the most important thing we need to learn first?</strong>
      <br><br>
            - ¿Los administradores podrán identificar rápidamente productos con stock bajo, próximos a vencer o con condiciones de conservación riesgosas mediante un dashboard centralizado?
      <br><br>
      - ¿Los proveedores podrán consultar necesidades de reposición, revisar su disponibilidad y crear pedidos dirigidos a minimarkets sin depender de canales externos?
      <br><br>
      - ¿Los administradores comprenderán y confiarán en el flujo de revisión, aceptación o rechazo de pedidos antes de modificar el inventario?
      <br><br>
      - ¿Las alertas de vencimiento, stock bajo y conservación generarán acciones concretas o serán ignoradas?
      <br><br>
      - ¿La separación de funciones entre administrador y proveedor será suficientemente clara para evitar confusión sobre quién puede modificar inventario y quién puede generar o aprobar pedidos?
      <br><br>
      ¿El valor percibido de centralizar inventario, conservación y abastecimiento será suficiente para que minimarkets y proveedores consideren adoptar MarketGo?      
    </td>
    <td valign="top">
      <strong>What’s the least amount of work we need to do to learn the next most important thing?</strong>
      <br><br>
      - Crear un prototipo navegable del dashboard con datos ficticios pero realistas de inventario, lotes, vencimientos, temperatura, humedad y alertas.
      <br><br>
      - Probar el flujo principal de abastecimiento: identificar una necesidad de reposición, consultar disponibilidad, crear un pedido como proveedor y revisarlo como administrador.
      <br><br>
      - Simular pedidos pendientes para comprobar si el administrador entiende cómo aceptar o rechazar una propuesta y qué efecto tiene cada decisión sobre el inventario.
      <br><br>
      - Mostrar alertas simuladas de stock bajo, vencimiento y conservación para observar si el usuario reconoce su prioridad y realiza una acción adecuada.
      <br><br>
      - Probar perfiles diferenciados de administrador y proveedor para verificar si cada usuario comprende qué acciones puede realizar según su rol.
      <br><br>
      - Medir finalización de tareas, tiempo, errores, necesidad de asistencia y comprensión del estado de cada operación.
      <br><br>
      - Realizar entrevistas breves después de las pruebas para evaluar confianza, facilidad de uso, utilidad percibida, intención de adopción y disposición de pago.
    </td>
  </tr>
</table>

---

## 1.3. Segmentos objetivo.

La solución está dirigida a **dos segmentos objetivos principales** que participan directamente en la cadena de abastecimiento de productos orgánicos: **administradores de minimarkets y proveedores**.

Estos segmentos presentan necesidades de negocio diferentes. Por ello, la plataforma utiliza una infraestructura tecnológica compartida, pero ofrece dashboards, funcionalidades y permisos específicos para cada segmento.

Los roles operativos que puedan existir dentro de cada empresa forman parte de la estructura interna de cada segmento y no constituyen segmentos objetivos independientes.

### 1.3.1. Administradores de Minimarkets

| Dimensión | Detalle del perfil |
|---|---|
| **Perfil Demográfico** | Propietarios, administradores o responsables de pequeños y medianos minimarkets dedicados a la comercialización de productos orgánicos y alimentos frescos. Son responsables de supervisar las operaciones del establecimiento y tomar decisiones relacionadas con inventario, conservación y abastecimiento. |
| **Perfil Geográfico** | Negocios ubicados principalmente en zonas urbanas con demanda de productos orgánicos y necesidad de mantener un abastecimiento constante. El segmento inicial puede concentrarse en Lima Metropolitana. |
| **Perfil Psicográfico** | Personas orientadas a mantener la calidad y disponibilidad de sus productos, reducir pérdidas y mejorar la eficiencia de sus operaciones. Valoran soluciones sencillas que permitan controlar el inventario, anticipar necesidades de reposición y tomar decisiones basadas en información actualizada. |
| **Puntos de Dolor** | Pérdidas ocasionadas por deterioro o vencimiento, dificultad para controlar niveles de stock, lotes y fechas de vencimiento, falta de visibilidad sobre las condiciones de almacenamiento, situaciones de desabastecimiento y dificultad para gestionar y validar pedidos de abastecimiento provenientes de proveedores. |
| **Uso de Tecnología** | Utilizan herramientas digitales para administrar ventas, inventarios y comunicación con proveedores, aunque pueden depender de hojas de cálculo, aplicaciones de mensajería y sistemas independientes que no integran toda la información operativa. |

### 1.3.2. Proveedores de Productos Orgánicos

| Dimensión | Detalle del perfil |
|---|---|
| **Perfil Demográfico** | Empresas, productores, distribuidores o comerciantes mayoristas de productos orgánicos que abastecen a minimarkets. Sus representantes son responsables de gestionar el catálogo, productos, disponibilidad, lotes y pedidos de abastecimiento. |
| **Perfil Geográfico** | Proveedores ubicados en zonas productoras, centros de distribución o áreas comerciales que atienden a minimarkets y otros negocios comercializadores de productos orgánicos. |
| **Perfil Psicográfico** | Negocios orientados a mantener una disponibilidad eficiente de sus productos, generar pedidos de abastecimiento oportunamente y establecer relaciones comerciales duraderas con sus clientes. Valoran la organización, trazabilidad y visibilidad de sus operaciones de abastecimiento. |
| **Puntos de Dolor** | Dificultad para administrar productos y disponibilidad, generar pedidos de abastecimiento para diferentes minimarkets, falta de visibilidad sobre el estado de las operaciones, gestión fragmentada de productos y lotes, y dificultades para coordinar el abastecimiento y mantener actualizada la información de sus productos. |
| **Uso de Tecnología** | Utilizan herramientas digitales, hojas de cálculo y aplicaciones de comunicación para gestionar productos, clientes y pedidos, pero pueden carecer de una plataforma especializada que conecte directamente su disponibilidad de productos con las necesidades de los minimarkets y permita realizar seguimiento de los pedidos generados. |
