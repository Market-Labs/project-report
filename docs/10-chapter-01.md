# Capítulo I: Introducción

## 1.1. Startup Profile

### 1.1.1. Descripción de la Startup

Market-Labs es una startup tecnológica peruana de reciente creación, orientada al desarrollo de iniciativas empresariales basadas en tecnología e innovación. La organización nace con el propósito de identificar oportunidades de mejora en actividades comerciales y operativas, transformándolas en propuestas de valor que puedan generar beneficios económicos, sociales y ambientales.

Como empresa emergente, Market-Labs adopta un enfoque de innovación continua, característico de las startups, buscando validar sus ideas de negocio de manera progresiva y adaptarse a las necesidades de su mercado objetivo. Su modelo de desarrollo se basa en la identificación de problemas reales, la experimentación y la mejora constante de sus propuestas, priorizando la generación de valor antes que el crecimiento basado únicamente en estructuras empresariales tradicionales. En este sentido, Market-Labs aspira a consolidarse progresivamente como una empresa tecnológica capaz de identificar nuevas oportunidades de negocio y desarrollar propuestas innovadoras que respondan a necesidades concretas del mercado. Su crecimiento se plantea mediante la generación de productos y servicios digitales escalables, procurando establecer relaciones sostenibles con sus clientes y demás actores relacionados con sus actividades empresariales.

**Misión:** Desarrollar iniciativas tecnológicas innovadoras que permitan atender necesidades reales del mercado, generando valor para los usuarios y contribuyendo al desarrollo de actividades empresariales más eficientes y sostenibles.

**Visión:** Consolidarse como una startup tecnológica peruana reconocida por su capacidad de innovación, adaptación y generación de propuestas digitales escalables que respondan a los nuevos desafíos del mercado.

**Valores:** Innovación, eficiencia, sostenibilidad, transparencia, adaptabilidad y orientación al usuario.

### 1.1.2. Perfiles de integrantes del equipo

> **Plantilla:** completar los datos de cada integrante y reemplazar la ruta de la imagen por la fotografía correspondiente.

| Imagen | Apellidos y nombres | Código | Carrera | Perfil |
|:---:|:---|:---:|:---|:---|
| <img src="./assets/chapter-01/profile_caceres.png" alt="Foto de Albino Caceres" width="120" /> | **Cáceres Pizarro, Albino Florencio** | U201923820 | Ingeniería de Software | Me considero una persona responsable y proactiva que le gusta trabajar en equipo. Además, siempre estoy abierto a ayudar, en lo posible, a cualquier integrante del equipo. Además, busco adaptarme rápidamente a los diversos retos que se presentan en el ciclo. |
| `<img src="./assets/chapter-01/[FOTO_INTEGRANTE_2]" alt="Foto de [NOMBRE_INTEGRANTE_2]" width="120" />` | **[APELLIDOS, NOMBRES]** | [CÓDIGO] | Ingeniería de Software | [Describir brevemente su formación, habilidades técnicas, fortalezas personales y aporte al proyecto.] |
| `<img src="./assets/chapter-01/[FOTO_INTEGRANTE_3]" alt="Foto de [NOMBRE_INTEGRANTE_3]" width="120" />` | **[APELLIDOS, NOMBRES]** | [CÓDIGO] | Ingeniería de Software | [Describir brevemente su formación, habilidades técnicas, fortalezas personales y aporte al proyecto.] |
| `<img src="./assets/chapter-01/[FOTO_INTEGRANTE_4]" alt="Foto de [NOMBRE_INTEGRANTE_4]" width="120" />` | **[APELLIDOS, NOMBRES]** | [CÓDIGO] | Ingeniería de Software | [Describir brevemente su formación, habilidades técnicas, fortalezas personales y aporte al proyecto.] |
| `<img src="./assets/chapter-01/[FOTO_INTEGRANTE_5]" alt="Foto de [NOMBRE_INTEGRANTE_5]" width="120" />` | **[APELLIDOS, NOMBRES]** | [CÓDIGO] | Ingeniería de Software | [Describir brevemente su formación, habilidades técnicas, fortalezas personales y aporte al proyecto.] |

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

### 1.2.2. Lean UX Process

#### 1.2.2.1. Lean UX Problem Statements

Los administradores de minimarkets que comercializan productos orgánicos necesitan mantener un control constante sobre sus inventarios, lotes, fechas de vencimiento y condiciones de almacenamiento. Sin embargo, la información puede encontrarse fragmentada entre diferentes registros y herramientas, dificultando la identificación temprana de productos en riesgo.

La ausencia de monitoreo integrado de las condiciones ambientales también limita la capacidad de los responsables para reaccionar oportunamente ante variaciones de temperatura o humedad que puedan afectar la conservación de los productos.

Paralelamente, los administradores de minimarkets necesitan conocer la disponibilidad de productos ofrecidos por los proveedores para realizar pedidos de abastecimiento. Los proveedores, por su parte, necesitan disponer de un mecanismo que les permita generar pedidos y consultar el estado de las operaciones realizadas.

Como consecuencia, pueden producirse pérdidas por deterioro, vencimiento, errores en pedidos, retrasos en el abastecimiento y situaciones de desabastecimiento.

Ante esto nos surge la siguiente pregunta:

**¿Cómo podría una plataforma web centralizar la gestión de inventarios, conservación y abastecimiento de productos orgánicos, utilizando un dashboard común con permisos diferenciados, para reducir pérdidas y mejorar la coordinación entre administradores de minimarkets y proveedores?**

1. **Domain:** Gestión, conservación y abastecimiento de productos orgánicos.

2. **Customer Segments:** Administradores de minimarkets y proveedores de productos orgánicos.

3. **Pain Points:** Pérdidas por deterioro o vencimiento, falta de visibilidad sobre las condiciones de almacenamiento, dificultades para controlar lotes y problemas de coordinación durante el abastecimiento.

4. **Gap:** Falta de una plataforma especializada que integre inventario, lotes, conservación y abastecimiento mediante un dashboard común con permisos adecuados para cada tipo de usuario.

5. **Vision/Strategy:** Centralizar digitalmente la información operativa y proporcionar herramientas que permitan identificar riesgos, gestionar inventarios y facilitar el abastecimiento mediante permisos diferenciados según el rol.

6. **Initial Segment:** Administradores de minimarkets y proveedores de productos orgánicos que requieran mejorar el control de inventarios, conservación y coordinación de abastecimiento.

---

#### 1.2.2.2. Lean UX Assumptions

**Business Assumptions:**

1. Se considera que los administradores de minimarkets necesitan mejorar el control de sus productos orgánicos para reducir pérdidas asociadas al deterioro y vencimiento.

2. Se plantea que una plataforma centralizada puede mejorar la visibilidad sobre inventarios, lotes, vencimientos y condiciones de almacenamiento.

3. Se considera que los proveedores necesitan una herramienta que les permita consultar los productos disponibles y generar pedidos de abastecimiento dirigidos a los minimarkets.

4. Se asume que la integración entre minimarkets y proveedores permitirá mejorar la eficiencia del proceso de abastecimiento.

5. Se considera que las alertas generadas a partir de las condiciones de conservación permitirán identificar oportunamente productos o lotes en riesgo.

6. Se plantea que la centralización de los pedidos permitirá mejorar la trazabilidad de las operaciones de abastecimiento entre compradores y proveedores.

7. Se estima que un modelo SaaS puede facilitar el acceso de pequeñas y medianas empresas a las funcionalidades de la plataforma sin requerir infraestructura tecnológica propia.

8. Se considera que la principal diferenciación de la solución será integrar en una misma plataforma la gestión de inventarios, conservación y abastecimiento de productos orgánicos.

9. Se asume que la plataforma podrá evolucionar posteriormente para incorporar sensores IoT reales y modelos de Machine Learning.

10. Se presume que uno de los principales riesgos de adopción será la resistencia de los usuarios a reemplazar procesos manuales y herramientas informales.

11. Se plantea que un dashboard común con permisos diferenciados permitirá mantener una experiencia consistente, evitando mostrar o permitir acciones que no correspondan al rol de cada usuario.

12. Se considera que la viabilidad del producto dependerá de que los beneficios obtenidos mediante la reducción de pérdidas y mejora del abastecimiento sean percibidos como superiores al costo de la solución.

**Business Outcome Assumptions**

1. Reducir la cantidad de productos dados de baja como consecuencia de condiciones inadecuadas de almacenamiento.

2. Incrementar la trazabilidad de los lotes y fechas de vencimiento gestionados por los minimarkets.

3. Reducir el tiempo necesario para identificar productos o lotes en condiciones de riesgo.

4. Mejorar la disponibilidad de información para la toma de decisiones relacionadas con el abastecimiento.

5. Incrementar la trazabilidad de los pedidos desde su creación hasta su aceptación y posterior incorporación al inventario.

**User Assumptions**

1. Los administradores de minimarkets necesitan visualizar rápidamente el estado de su inventario y los productos próximos a vencer.

2. Los administradores de minimarkets valoran recibir alertas cuando las condiciones de almacenamiento puedan afectar determinados productos.

3. Los administradores de minimarkets necesitan consultar la disponibilidad de productos y lotes ofrecidos por los proveedores.

4. Los proveedores necesitan consultar los productos que ofrecen y generar pedidos de abastecimiento desde un único sistema.

5. Los proveedores necesitan consultar el estado de los pedidos realizados y de las operaciones asociadas a los productos ofrecidos.

6. Ambos segmentos necesitan consultar el estado de un pedido y disponer de información centralizada sobre las operaciones de abastecimiento.

**User Outcome Assumptions**

1. Los administradores de minimarkets tendrán mayor confianza en la información de su inventario al disponer de un registro centralizado de productos, lotes y vencimientos.

2. Los administradores de minimarkets podrán identificar oportunamente condiciones ambientales anómalas que puedan representar un riesgo para los productos.

3. Los administradores de minimarkets podrán consultar productos disponibles y gestionar pedidos de abastecimiento desde la plataforma.

4. Los proveedores podrán generar pedidos y consultar el estado de sus operaciones sin modificar directamente el inventario del minimarket.

5. Los usuarios experimentarán una reducción de la incertidumbre respecto al estado de los pedidos y operaciones de abastecimiento.

6. Los administradores de minimarkets podrán mantener actualizado su inventario de forma más eficiente al incorporar automáticamente los productos correspondientes cuando acepten un pedido.

---

#### 1.2.2.3. Lean UX Hypothesis Statements

**Hypothesis 1**

Creemos que al centralizar la gestión de inventarios, lotes y fechas de vencimiento de los minimarkets, facilitaremos la identificación de productos próximos a vencer. Lo sabremos cuando los administradores puedan identificar los productos críticos desde el dashboard sin necesidad de consultar diferentes registros.

**Hypothesis 2**

Creemos que al implementar un sistema de monitoreo de temperatura y humedad, acompañado de alertas basadas en los requisitos de conservación de cada producto, mejoraremos la capacidad de los administradores para detectar condiciones de riesgo. Lo sabremos cuando puedan identificar y atender oportunamente las alertas generadas.

**Hypothesis 3**

Creemos que al permitir que los proveedores consulten productos disponibles y generen pedidos de abastecimiento desde el mismo dashboard, facilitaremos la coordinación de las operaciones entre proveedores y minimarkets. Lo sabremos cuando los proveedores puedan realizar pedidos y consultar su estado sin utilizar canales externos de comunicación.

**Hypothesis 4**

Creemos que al centralizar el ciclo de vida de los pedidos y automatizar la incorporación de los productos al inventario después de su aceptación, reduciremos los errores y el tiempo necesario para actualizar el inventario. Lo sabremos cuando los administradores puedan aceptar un pedido y visualizar automáticamente los productos correspondientes en su inventario.

**Hypothesis 5**

Creemos que al utilizar un dashboard común con permisos diferenciados para administradores de minimarkets y proveedores, facilitaremos el uso de la plataforma y mantendremos la seguridad de la información. Lo sabremos cuando cada usuario pueda acceder a la información y ejecutar únicamente las acciones correspondientes a su rol.

---

#### 1.2.2.4. Lean UX Canvas

<table>
  <tr>
    <td valign="top">
      <strong>Business problem</strong>
      <br><br>
      Los administradores de minimarkets y proveedores de productos orgánicos gestionan inventarios, lotes, conservación y abastecimiento mediante procesos que pueden encontrarse fragmentados.
      <br><br>
      Esta falta de centralización dificulta identificar productos en riesgo, controlar vencimientos, conocer la disponibilidad de productos y realizar seguimiento de los pedidos.
      <br><br>
      Como consecuencia, pueden generarse pérdidas por deterioro o vencimiento, errores de abastecimiento y dificultades de coordinación entre compradores y proveedores.
    </td>
    <td rowspan="2" valign="top">
      <strong>Solution ideas</strong>
      <br><br>
      - Plataforma web especializada en productos orgánicos
      <br><br>
      - Dashboard común con permisos diferenciados según el tipo de usuario
      <br><br>
      - Gestión de inventarios, ubicaciones, lotes y vencimientos
      <br><br>
      - Monitoreo de temperatura y humedad mediante datos simulados
      <br><br>
      - Sistema de alertas para productos y lotes en riesgo
      <br><br>
      - Gestión de mermas y donaciones
      <br><br>
      - Consulta de productos y disponibilidad de proveedores
      <br><br>
      - Generación y seguimiento de pedidos de abastecimiento
      <br><br>
      - Incorporación automática de productos al inventario después de la aceptación del pedido
    </td>
    <td valign="top">
      <strong>Business Outcomes</strong>
      <br><br>
      - Reducir pérdidas asociadas al deterioro y vencimiento
      <br><br>
      - Mejorar la trazabilidad de productos y lotes
      <br><br>
      - Mejorar la eficiencia del abastecimiento
      <br><br>
      - Incrementar la visibilidad sobre el estado de pedidos y operaciones
      <br><br>
      - Centralizar la información operativa de minimarkets y proveedores
    </td>
  </tr>
  <tr>
    <td valign="top">
      <strong>Users and customers</strong>
      <br><br>
      - Administradores de minimarkets
      <br>
      - Proveedores de productos orgánicos
    </td>
    <td valign="top">
      <strong>User benefits</strong>
      <br><br>
      - Mayor visibilidad del inventario
      <br><br>
      - Identificación temprana de productos en riesgo
      <br><br>
      - Control centralizado de lotes y vencimientos
      <br><br>
      - Consulta de productos disponibles
      <br><br>
      - Generación y seguimiento de pedidos
      <br><br>
      - Actualización automática del inventario después de aceptar pedidos
    </td>
  </tr>
  <tr>
    <td valign="top">
      <strong>Hypotheses</strong>
      <br><br>
      - Si se centraliza el inventario y los lotes, se facilitará la identificación de productos próximos a vencer.
      <br><br>
      - Si se implementan alertas basadas en temperatura y humedad, se detectarán oportunamente condiciones de riesgo.
      <br><br>
      - Si los proveedores pueden generar pedidos desde la plataforma, se facilitará la coordinación del abastecimiento.
      <br><br>
      - Si los pedidos aceptados actualizan automáticamente el inventario, se reducirán errores y tareas manuales.
      <br><br>
      - Si cada rol cuenta con permisos específicos dentro de un dashboard común, se facilitará el uso y se protegerá la información.
    </td>
    <td valign="top">
      <strong>What’s the most important thing we need to learn first?</strong>
      <br><br>
      Si los administradores de minimarkets y proveedores perciben suficiente valor en una plataforma integrada de gestión de inventario, conservación y abastecimiento como para incorporarla a sus procesos operativos.
    </td>
    <td valign="top">
      <strong>What’s the least amount of work we need to do to learn the next most important thing?</strong>
      <br><br>
      Realizar entrevistas con administradores de minimarkets y proveedores y validar mediante un prototipo de baja fidelidad los flujos principales de inventario, alertas, consulta de productos, generación de pedidos y actualización automática del inventario.
    </td>
  </tr>
</table>

---

## 1.3. Segmentos Objetivos

La solución está dirigida a **dos segmentos objetivos principales** que participan directamente en la cadena de abastecimiento de productos orgánicos: **administradores de minimarkets y proveedores**.

Estos segmentos representan dos tipos de organizaciones con necesidades de negocio diferentes. Por ello, la plataforma utiliza un **dashboard común**, pero aplica permisos específicos para cada segmento. Los administradores de minimarkets cuentan con permisos de lectura y escritura sobre la información de su operación, mientras que los proveedores cuentan con permisos de consulta y acciones específicas para generar pedidos, sin acceso para modificar directamente el inventario del minimarket.

Los roles operativos que puedan existir dentro de cada empresa forman parte de la estructura interna de cada segmento y no constituyen segmentos objetivos independientes.

### 1.3.1. Administradores de Minimarkets

| Dimensión | Detalle del perfil |
|---|---|
| **Perfil Demográfico** | Propietarios, administradores o responsables de pequeños y medianos minimarkets dedicados a la comercialización de productos orgánicos y alimentos frescos. Son responsables de supervisar las operaciones comerciales y tomar decisiones relacionadas con inventario, conservación y abastecimiento. |
| **Perfil Geográfico** | Negocios ubicados principalmente en zonas urbanas con demanda de productos orgánicos y necesidad de mantener un abastecimiento constante. El segmento inicial puede concentrarse en Lima Metropolitana. |
| **Perfil Psicográfico** | Personas orientadas a mantener la calidad de sus productos, reducir pérdidas y asegurar la disponibilidad constante de mercadería. Valoran soluciones sencillas que permitan controlar las operaciones del negocio y tomar decisiones basadas en información actualizada. |
| **Puntos de Dolor** | Pérdidas ocasionadas por deterioro o vencimiento de productos, dificultad para controlar lotes y fechas de vencimiento, falta de visibilidad sobre las condiciones de almacenamiento, desabastecimiento y dificultad para coordinar pedidos con proveedores. |
| **Uso de Tecnología** | Utilizan herramientas digitales para administrar ventas, inventarios y comunicación con proveedores, aunque pueden depender de hojas de cálculo, aplicaciones de mensajería y sistemas independientes que no integran toda la información operativa. |

### 1.3.2. Proveedores

| Dimensión | Detalle del perfil |
|---|---|
| **Perfil Demográfico** | Empresas, productores, distribuidores o comerciantes mayoristas de productos orgánicos que abastecen a minimarkets. Sus representantes participan en la oferta de productos y en las operaciones de abastecimiento realizadas mediante la plataforma. |
| **Perfil Geográfico** | Proveedores ubicados en zonas productoras, centros de distribución o áreas comerciales que atienden a minimarkets y otros negocios comercializadores de productos orgánicos. |
| **Perfil Psicográfico** | Negocios orientados a mantener una relación comercial eficiente con sus clientes y facilitar el abastecimiento oportuno de productos. Valoran la trazabilidad, organización y visibilidad de las operaciones relacionadas con los productos que ofrecen. |
| **Puntos de Dolor** | Dificultad para mantener visibilidad sobre los pedidos realizados, falta de centralización de la información de las operaciones comerciales y dependencia de diferentes canales de comunicación para coordinar el abastecimiento. |
| **Uso de Tecnología** | Utilizan herramientas digitales, hojas de cálculo y aplicaciones de comunicación para gestionar sus operaciones comerciales, pero pueden carecer de una plataforma especializada que centralice la información de los productos ofrecidos y los pedidos realizados por los minimarkets. |

