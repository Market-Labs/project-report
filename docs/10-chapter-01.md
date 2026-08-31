
# Capítulo I: Introducción

## 1.1. Startup Profile

### 1.1.1. Descripción de la Startup

**[NOMBRE DE LA STARTUP]** es una startup tecnológica orientada al desarrollo de soluciones digitales para la gestión eficiente de productos orgánicos. Su propuesta busca conectar la operación de los **minimarkets y proveedores** mediante una plataforma web que centraliza la gestión de inventarios, lotes, pedidos, abastecimiento y trazabilidad de los productos.

La solución aborda principalmente los problemas asociados al deterioro y pérdida de productos orgánicos, la falta de visibilidad sobre las condiciones de almacenamiento y las dificultades para mantener un abastecimiento oportuno. Para ello, la plataforma integra la gestión transaccional con capacidades de monitoreo de temperatura y humedad mediante datos simulados, permitiendo generar alertas cuando las condiciones de conservación representan un riesgo para determinados productos o lotes.

La plataforma contempla dos segmentos de negocio diferenciados: **minimarkets y proveedores**. Ambos comparten una infraestructura tecnológica común, autenticación, comunicación, notificaciones y gestión de pedidos, pero cuentan con dashboards, funcionalidades y permisos específicos de acuerdo con sus necesidades operativas.

**Misión:** Facilitar la gestión y conservación de productos orgánicos mediante herramientas digitales que permitan a minimarkets y proveedores mejorar la trazabilidad, reducir pérdidas y optimizar sus procesos de abastecimiento.

**Visión:** Convertirse en una plataforma tecnológica de referencia para la gestión inteligente y sostenible de productos orgánicos, conectando a los diferentes actores de la cadena de abastecimiento.

**Valores:** Trazabilidad, eficiencia, sostenibilidad, transparencia, innovación y orientación al usuario.

### 1.1.2. Perfiles de integrantes del equipo

> **Plantilla:** completar los datos de cada integrante y reemplazar la ruta de la imagen por la fotografía correspondiente.

| Imagen | Apellidos y nombres | Código | Carrera | Perfil |
|:---:|:---|:---:|:---|:---|
| `<img src="./assets/chapter-01/[FOTO_INTEGRANTE_1]" alt="Foto de [NOMBRE_INTEGRANTE_1]" width="120" />` | **[APELLIDOS, NOMBRES]** | [CÓDIGO] | Ingeniería de Software | [Describir brevemente su formación, habilidades técnicas, fortalezas personales y aporte al proyecto.] |
| `<img src="./assets/chapter-01/[FOTO_INTEGRANTE_2]" alt="Foto de [NOMBRE_INTEGRANTE_2]" width="120" />` | **[APELLIDOS, NOMBRES]** | [CÓDIGO] | Ingeniería de Software | [Describir brevemente su formación, habilidades técnicas, fortalezas personales y aporte al proyecto.] |
| `<img src="./assets/chapter-01/[FOTO_INTEGRANTE_3]" alt="Foto de [NOMBRE_INTEGRANTE_3]" width="120" />` | **[APELLIDOS, NOMBRES]** | [CÓDIGO] | Ingeniería de Software | [Describir brevemente su formación, habilidades técnicas, fortalezas personales y aporte al proyecto.] |
| `<img src="./assets/chapter-01/[FOTO_INTEGRANTE_4]" alt="Foto de [NOMBRE_INTEGRANTE_4]" width="120" />` | **[APELLIDOS, NOMBRES]** | [CÓDIGO] | Ingeniería de Software | [Describir brevemente su formación, habilidades técnicas, fortalezas personales y aporte al proyecto.] |
| `<img src="./assets/chapter-01/[FOTO_INTEGRANTE_5]" alt="Foto de [NOMBRE_INTEGRANTE_5]" width="120" />` | **[APELLIDOS, NOMBRES]** | [CÓDIGO] | Ingeniería de Software | [Describir brevemente su formación, habilidades técnicas, fortalezas personales y aporte al proyecto.] |

---

## 1.2. Solution Profile

Nuestra solución, **[NOMBRE DEL PRODUCTO]**, es una plataforma web orientada a la gestión, conservación y abastecimiento de productos orgánicos. La solución conecta a minimarkets y proveedores dentro de un mismo ecosistema digital, permitiendo administrar inventarios, lotes, pedidos, entregas y condiciones de almacenamiento desde una plataforma centralizada.

Para los minimarkets, la plataforma permite controlar el inventario propio, gestionar lotes y fechas de vencimiento, monitorear las condiciones ambientales de almacenamiento, recibir alertas sobre productos en riesgo y gestionar procesos de merma o donación. Asimismo, permite consultar la disponibilidad de productos de proveedores conectados y generar pedidos de abastecimiento.

Para los proveedores, la plataforma permite publicar productos y lotes disponibles, establecer precios por volumen, gestionar su inventario, atender pedidos provenientes de diferentes minimarkets y realizar el seguimiento de los despachos y entregas.

La solución busca reducir las pérdidas asociadas al deterioro de productos orgánicos y mejorar la coordinación entre compradores y proveedores mediante información centralizada, trazabilidad y flujos de trabajo diferenciados para cada segmento.

### 1.2.1. Antecedentes y problemática

Los productos orgánicos presentan una mayor sensibilidad a factores como la temperatura, humedad, manipulación y tiempo de almacenamiento. Cuando estas condiciones no son controladas adecuadamente, aumenta el riesgo de deterioro y, como consecuencia, se generan pérdidas económicas, desperdicio de alimentos y disminución de la disponibilidad de productos para los consumidores.

En los minimarkets, uno de los principales desafíos consiste en mantener un control adecuado sobre los productos almacenados, sus lotes y fechas de vencimiento. La ausencia de mecanismos centralizados de seguimiento puede dificultar la identificación temprana de productos en riesgo y provocar que estos sean detectados cuando ya no pueden comercializarse.

A esta problemática se suma la necesidad de mantener condiciones apropiadas de conservación. El monitoreo manual o fragmentado de variables como temperatura y humedad limita la capacidad de los responsables del establecimiento para identificar oportunamente situaciones anómalas que puedan afectar determinados productos.

Por otro lado, el abastecimiento representa un segundo desafío. Los minimarkets necesitan conocer qué productos y lotes se encuentran disponibles en los proveedores para realizar pedidos oportunamente, mientras que los proveedores necesitan gestionar múltiples pedidos provenientes de diferentes clientes sin perder trazabilidad sobre el estado de cada operación.

Esta situación genera una fragmentación de información entre inventarios, pedidos, entregas e incidencias. La utilización de herramientas no especializadas puede dificultar la coordinación entre ambas partes y aumentar el riesgo de errores, retrasos y pérdidas de productos.

Ante este escenario, se propone una plataforma digital que centralice la información de inventarios, lotes, conservación y abastecimiento, manteniendo separados los procesos de negocio de minimarkets y proveedores, pero conectándolos mediante el flujo de pedidos.

**Técnica "The 5W's y 2H's" aplicada al problema:**

| The 5W's y 2H's | Pregunta | Descripción |
|:---|:---|:---|
| **Who** | ¿Quiénes están involucrados? | Minimarkets responsables de almacenar y comercializar productos orgánicos y proveedores encargados de producir, almacenar y abastecer dichos productos. |
| **What** | ¿Cuál es el problema? | Dificultad para gestionar de manera integrada el inventario, conservación, lotes, vencimientos y abastecimiento de productos orgánicos, generando riesgo de pérdidas y desabastecimiento. |
| **Where** | ¿Dónde ocurre? | Principalmente en los procesos de almacenamiento y comercialización de productos orgánicos en minimarkets, así como en la gestión de inventarios y pedidos de los proveedores. |
| **When** | ¿Cuándo sucede? | Durante el almacenamiento, seguimiento de lotes, control de fechas de vencimiento y procesos de abastecimiento y entrega de productos. |
| **Why** | ¿Por qué sucede? | Debido a la fragmentación de la información, utilización de procesos manuales y ausencia de una plataforma especializada que conecte inventario, conservación y abastecimiento. |
| **How** | ¿Cómo se manifiesta? | Mediante dificultades para identificar productos en riesgo, controlar lotes y vencimientos, conocer disponibilidad de proveedores, realizar pedidos y dar seguimiento a entregas e incidencias. |
| **How Much** | ¿Cuánto impacto tiene? | El problema puede traducirse en pérdidas económicas por productos deteriorados o vencidos, desperdicio de alimentos, interrupciones en el abastecimiento y mayores costos operativos. |

---

### 1.2.2. Lean UX Process

#### 1.2.2.1. Lean UX Problem Statements

Los minimarkets que comercializan productos orgánicos necesitan mantener un control constante sobre sus inventarios, lotes, fechas de vencimiento y condiciones de almacenamiento. Sin embargo, la información puede encontrarse fragmentada entre diferentes registros y herramientas, dificultando la identificación temprana de productos en riesgo.

La ausencia de monitoreo integrado de las condiciones ambientales también limita la capacidad de los responsables para reaccionar oportunamente ante variaciones de temperatura o humedad que puedan afectar la conservación de los productos.

Paralelamente, los minimarkets necesitan mantener una comunicación eficiente con sus proveedores para conocer la disponibilidad de productos y realizar pedidos de abastecimiento, mientras que los proveedores necesitan administrar pedidos de múltiples clientes y mantener la trazabilidad de sus despachos.

Como consecuencia, pueden producirse pérdidas por deterioro, vencimiento, errores en pedidos, retrasos en entregas y situaciones de desabastecimiento.

Ante esto nos surge la siguiente pregunta:

**¿Cómo podría una plataforma web centralizar la gestión de inventarios, conservación y abastecimiento de productos orgánicos para reducir pérdidas y mejorar la coordinación entre minimarkets y proveedores?**

1. **Domain:** Gestión, conservación y abastecimiento de productos orgánicos.

2. **Customer Segments:** Minimarkets y proveedores de productos orgánicos.

3. **Pain Points:** Pérdidas por deterioro o vencimiento, falta de visibilidad sobre las condiciones de almacenamiento, dificultades para controlar lotes y problemas de coordinación durante el abastecimiento.

4. **Gap:** Falta de una plataforma especializada que integre inventario, lotes, conservación y abastecimiento entre minimarkets y proveedores.

5. **Vision/Strategy:** Centralizar digitalmente la información operativa y proporcionar herramientas que permitan identificar riesgos, gestionar inventarios y facilitar el abastecimiento.

6. **Initial Segment:** Minimarkets y proveedores de productos orgánicos que requieran mejorar el control de inventarios y la coordinación de abastecimiento.

#### 1.2.2.2. Lean UX Assumptions

**Business Assumptions:**

1. Se considera que los minimarkets necesitan mejorar el control de sus productos orgánicos para reducir pérdidas asociadas al deterioro y vencimiento.

2. Se plantea que una plataforma centralizada puede mejorar la visibilidad sobre inventarios, lotes, vencimientos y condiciones de almacenamiento.

3. Se considera que los proveedores necesitan una herramienta especializada para gestionar productos, lotes, disponibilidad y pedidos provenientes de diferentes minimarkets.

4. Se asume que la integración entre minimarkets y proveedores permitirá mejorar la eficiencia del proceso de abastecimiento.

5. Se considera que las alertas generadas a partir de las condiciones de conservación permitirán identificar oportunamente productos o lotes en riesgo.

6. Se plantea que la centralización de los pedidos permitirá mejorar la trazabilidad de las operaciones comerciales entre compradores y proveedores.

7. Se estima que un modelo SaaS puede facilitar el acceso de pequeñas y medianas empresas a las funcionalidades de la plataforma sin requerir infraestructura tecnológica propia.

8. Se considera que la principal diferenciación de la solución será integrar en una misma plataforma la gestión de inventarios, conservación y abastecimiento de productos orgánicos.

9. Se asume que la plataforma podrá evolucionar posteriormente para incorporar sensores IoT reales y modelos de Machine Learning.

10. Se presume que uno de los principales riesgos de adopción será la resistencia de los usuarios a reemplazar procesos manuales y herramientas informales.

11. Se plantea que una interfaz sencilla y dashboards diferenciados permitirán reducir la complejidad para cada tipo de usuario.

12. Se considera que la viabilidad del producto dependerá de que los beneficios obtenidos mediante la reducción de pérdidas y mejora del abastecimiento sean percibidos como superiores al costo de la solución.

**Business Outcome Assumptions**

1. Reducir la cantidad de productos dados de baja como consecuencia de condiciones inadecuadas de almacenamiento.

2. Incrementar la trazabilidad de los lotes y fechas de vencimiento gestionados por los minimarkets.

3. Reducir el tiempo necesario para identificar productos o lotes en condiciones de riesgo.

4. Mejorar la disponibilidad de información para la toma de decisiones relacionadas con el abastecimiento.

5. Incrementar la trazabilidad de los pedidos desde su creación hasta la recepción o despacho.

**User Assumptions**

1. Los responsables de minimarkets necesitan visualizar rápidamente el estado de su inventario y los productos próximos a vencer.

2. Los responsables de minimarkets valoran recibir alertas cuando las condiciones de almacenamiento puedan afectar determinados productos.

3. Los encargados de abastecimiento necesitan consultar la disponibilidad de productos y lotes de proveedores conectados.

4. Los proveedores necesitan visualizar y gestionar los pedidos recibidos de diferentes minimarkets desde un único sistema.

5. Los proveedores requieren controlar la disponibilidad de sus lotes y establecer precios de acuerdo con el volumen solicitado.

6. Ambos segmentos necesitan consultar el estado de un pedido y comunicarse respecto a incidencias asociadas a la operación.

**User Outcome Assumptions**

1. Los responsables de minimarkets tendrán mayor confianza en la información de su inventario al disponer de un registro centralizado de productos, lotes y vencimientos.

2. Los responsables de almacenamiento podrán identificar oportunamente condiciones ambientales anómalas que puedan representar un riesgo para los productos.

3. Los encargados de abastecimiento podrán encontrar productos disponibles en proveedores conectados sin depender de múltiples canales de comunicación.

4. Los proveedores podrán administrar sus pedidos de manera más organizada y mantener trazabilidad sobre cada operación.

5. Los usuarios experimentarán una reducción de la incertidumbre respecto al estado de los pedidos y entregas.

6. Los responsables de los negocios podrán tomar decisiones operativas con mayor rapidez al contar con información centralizada y actualizada.

#### 1.2.2.3. Lean UX Hypothesis Statements

**Hypothesis 1**

Creemos que al centralizar la gestión de inventarios, lotes y fechas de vencimiento de los minimarkets, facilitaremos la identificación de productos próximos a vencer. Lo sabremos cuando los usuarios puedan identificar los productos críticos desde el dashboard sin necesidad de consultar diferentes registros.

**Hypothesis 2**

Creemos que al implementar un sistema de monitoreo de temperatura y humedad, acompañado de alertas basadas en los requisitos de conservación de cada producto, mejoraremos la capacidad de los responsables para detectar condiciones de riesgo. Lo sabremos cuando los usuarios puedan identificar y atender oportunamente las alertas generadas.

**Hypothesis 3**

Creemos que al conectar la disponibilidad de productos y lotes de los proveedores con los minimarkets, reduciremos el tiempo necesario para encontrar productos disponibles para abastecimiento. Lo sabremos cuando los usuarios puedan localizar y seleccionar productos de proveedores conectados desde la plataforma.

**Hypothesis 4**

Creemos que al centralizar el ciclo de vida de los pedidos, reduciremos la incertidumbre sobre el estado de las operaciones de abastecimiento. Lo sabremos cuando minimarkets y proveedores puedan consultar el estado actualizado de cada pedido sin utilizar canales externos de comunicación.

**Hypothesis 5**

Creemos que al proporcionar dashboards diferenciados para minimarkets y proveedores, mejoraremos la experiencia de cada segmento al mostrar únicamente las funcionalidades y métricas relevantes para su operación. Lo sabremos cuando los usuarios puedan completar sus principales tareas sin acceder a funcionalidades que no correspondan a su perfil de negocio.

#### 1.2.2.4. Lean UX Canvas

<table>
  <tr>
    <td valign="top">
      <strong>Business problem</strong>
      <br><br>
      Los minimarkets y proveedores de productos orgánicos gestionan inventarios, lotes, conservación y abastecimiento mediante procesos que pueden encontrarse fragmentados.
      <br><br>
      Esta falta de centralización dificulta identificar productos en riesgo, controlar vencimientos, conocer disponibilidad de proveedores y realizar seguimiento de los pedidos.
      <br><br>
      Como consecuencia, pueden generarse pérdidas por deterioro o vencimiento, errores de abastecimiento y dificultades de coordinación entre compradores y proveedores.
    </td>
    <td rowspan="2" valign="top">
      <strong>Solution ideas</strong>
      <br><br>
      - Plataforma web especializada en productos orgánicos
      <br><br>
      - Dashboard diferenciado para minimarkets y proveedores
      <br><br>
      - Gestión de inventarios, ubicaciones, lotes y vencimientos
      <br><br>
      - Monitoreo de temperatura y humedad mediante datos simulados
      <br><br>
      - Sistema de alertas para productos y lotes en riesgo
      <br><br>
      - Gestión de mermas y donaciones
      <br><br>
      - Catálogo y disponibilidad de productos por lote
      <br><br>
      - Gestión y seguimiento de pedidos y entregas
      <br><br>
      - Mensajería e incidencias asociadas a transacciones
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
      - Incrementar la visibilidad sobre el estado de pedidos y entregas
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
      - Encargados de inventario
      <br>
      - Responsables de abastecimiento
      <br>
      - Administradores de proveedores
      <br>
      - Responsables de almacén y despacho
      <br>
      - Empresas comercializadoras y proveedoras de productos orgánicos
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
      - Consulta de disponibilidad de proveedores
      <br><br>
      - Seguimiento de pedidos y entregas
      <br><br>
      - Mejor coordinación entre compradores y proveedores
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
      - Si se conecta la disponibilidad de proveedores con los minimarkets, se facilitará el abastecimiento.
      <br><br>
      - Si se centraliza el ciclo de vida de los pedidos, se reducirá la incertidumbre sobre las operaciones.
      <br><br>
      - Si cada segmento cuenta con un dashboard especializado, se facilitará la ejecución de sus tareas principales.
    </td>
    <td valign="top">
      <strong>What’s the most important thing we need to learn first?</strong>
      <br><br>
      Si minimarkets y proveedores perciben suficiente valor en una plataforma integrada de gestión de inventario, conservación y abastecimiento como para incorporarla a sus procesos operativos.
    </td>
    <td valign="top">
      <strong>What’s the least amount of work we need to do to learn the next most important thing?</strong>
      <br><br>
      Realizar entrevistas con responsables de minimarkets y proveedores y validar mediante un prototipo de baja fidelidad los flujos principales de inventario, alertas, consulta de disponibilidad y gestión de pedidos.
    </td>
  </tr>
</table>

---

## 1.3. Segmentos Objetivos

La solución se dirige a dos segmentos de negocio complementarios dentro de la cadena de abastecimiento de productos orgánicos: **minimarkets y proveedores**.

A diferencia de una segmentación basada únicamente en roles internos, estos segmentos representan dos tipos de organizaciones con necesidades operativas diferentes. Por ello, la plataforma utiliza una infraestructura compartida, pero ofrece dashboards, funcionalidades y permisos específicos para cada segmento.

### 1.3.1. Minimarkets

| Dimensión | Detalle del perfil |
|---|---|
| **Perfil Demográfico** | Pequeñas y medianas empresas dedicadas a la comercialización de productos orgánicos y alimentos frescos. Sus usuarios pueden incluir administradores, encargados de inventario, responsables de abastecimiento y personal de ventas. |
| **Perfil Geográfico** | Negocios ubicados principalmente en zonas urbanas con demanda de productos orgánicos y necesidad de abastecimiento frecuente. El segmento inicial puede concentrarse en Lima Metropolitana. |
| **Perfil Psicográfico** | Negocios orientados a mantener la calidad de sus productos, reducir pérdidas y ofrecer disponibilidad constante a sus clientes. Valoran soluciones sencillas que permitan controlar sus operaciones sin incrementar significativamente la carga administrativa. |
| **Puntos de Dolor** | Pérdidas por deterioro o vencimiento, dificultad para controlar lotes, falta de visibilidad sobre condiciones de almacenamiento, desabastecimiento y dificultad para encontrar proveedores disponibles. |
| **Uso de Tecnología** | Utilizan herramientas digitales para ventas, inventario y comunicación, aunque pueden depender de soluciones independientes, hojas de cálculo o canales informales para coordinar pedidos con proveedores. |

### 1.3.2. Proveedores

| Dimensión | Detalle del perfil |
|---|---|
| **Perfil Demográfico** | Empresas o negocios dedicados a la producción, distribución o comercialización mayorista de productos orgánicos. Sus usuarios pueden incluir administradores, encargados de almacén, responsables comerciales y responsables de despacho. |
| **Perfil Geográfico** | Proveedores ubicados en zonas productoras o centros de distribución que atienden a minimarkets y otros negocios comercializadores de productos orgánicos. |
| **Perfil Psicográfico** | Empresas orientadas a mantener una rotación eficiente de sus lotes, atender pedidos oportunamente y establecer relaciones comerciales duraderas con sus clientes. Valoran la trazabilidad y el control sobre sus operaciones comerciales. |
| **Puntos de Dolor** | Dificultad para gestionar pedidos de múltiples clientes, falta de visibilidad sobre el estado de los pedidos, control fragmentado de lotes y disponibilidad, y necesidad de mejorar la coordinación de despachos. |
| **Uso de Tecnología** | Utilizan sistemas de gestión, hojas de cálculo y herramientas de comunicación digital para administrar inventarios y pedidos, pero pueden carecer de una solución especializada que conecte directamente su disponibilidad con los minimarkets. |
