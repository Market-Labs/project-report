# PlantillaDA

<!-- AUTO-DOCS:START -->

<div align="center">
<br>
<img src=".docs/assets/common/logo-upc.png" width="180" alt="Logo UPC">
<br><br>

# UNIVERSIDAD PERUANA DE CIENCIAS APLICADAS

<br>

### Facultad de Ingeniería

### Carrera de Ingeniería de Software

<br>

**Ciclo Académico 2026-2**

<br>

**Código:** 1ASI0730   |   **Curso:** Aplicaciones Web   |   **NRC:** 8130

<br>

**Docente:** Villafuerte Bazan, Oscar Ivan

<br>

# Informe de Trabajo Final - AV2

<br>

### **Nombre de la Startup:**

**startup**

<br>

### **Nombre del Producto:**

**ProductName**

<br>

### Relación de integrantes

<table align="center" style="margin: 0 auto; font-size: 15px;">
<thead>
    <tr>
      <th align="center">Código</th>
      <th align="center">Apellidos y Nombres</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center">U201923820</td>
      <td align="left">Cáceres Pizarro, Albino Florencio</td>
    </tr>
    <tr>
      <td align="center">U20231B504</td>
      <td align="left">[NOMBRE DEL INTEGRANTE 2]</td>
    </tr>
    <tr>
      <td align="center">U202316687</td>
      <td align="left">[NOMBRE DEL INTEGRANTE 3]</td>
    </tr>
    <tr>
      <td align="center">U202322849</td>
      <td align="left">[NOMBRE DEL INTEGRANTE 4]</td>
    </tr>
    <tr>
      <td align="center">U201923820</td>
      <td align="left">[NOMBRE DEL INTEGRANTE 5]</td>
    </tr>
  </tbody>
</table>

<br><br>

**Lima, agosto de 2026**

</div>

---

# Capítulo I: Introducción

## 1.1. Startup Profile

### 1.1.1. Descripción de la Startup

**Market-Labs** es una startup tecnológica orientada al desarrollo de soluciones digitales para la gestión eficiente de productos orgánicos. Su propuesta busca conectar a **administradores de minimarkets y proveedores** mediante una plataforma web que centraliza la gestión de inventarios, lotes, pedidos, abastecimiento y trazabilidad de los productos.

La solución aborda principalmente los problemas asociados al deterioro y pérdida de productos orgánicos, la falta de visibilidad sobre las condiciones de almacenamiento y las dificultades para mantener un abastecimiento oportuno. Para ello, la plataforma integra la gestión transaccional con capacidades de monitoreo de temperatura y humedad mediante datos simulados, permitiendo generar alertas cuando las condiciones de conservación representan un riesgo para determinados productos o lotes.

La plataforma contempla dos segmentos de negocio diferenciados: administradores de minimarkets y proveedores. Ambos comparten una infraestructura tecnológica común, autenticación, comunicación, notificaciones y gestión de pedidos, pero cuentan con dashboards, funcionalidades y permisos específicos de acuerdo con sus necesidades operativas.

Los administradores de minimarkets utilizan la plataforma principalmente para controlar sus inventarios, lotes, fechas de vencimiento, condiciones de almacenamiento, mermas, donaciones y procesos de abastecimiento. Por su parte, los proveedores utilizan la plataforma para gestionar sus productos, lotes disponibles, precios, inventario, pedidos recibidos y procesos de despacho y entrega.

**Misión:** Facilitar la gestión y conservación de productos orgánicos mediante herramientas digitales que permitan a administradores de minimarkets y proveedores mejorar la trazabilidad, reducir pérdidas y optimizar sus procesos de abastecimiento.

**Visión:** Convertirse en una plataforma tecnológica de referencia para la gestión inteligente y sostenible de productos orgánicos, conectando digitalmente a los principales actores de su cadena de abastecimiento.

**Valores:** Trazabilidad, eficiencia, sostenibilidad, transparencia, innovación y orientación al usuario.

### 1.1.2. Perfiles de integrantes del equipo

> **Plantilla:** completar los datos de cada integrante y reemplazar la ruta de la imagen por la fotografía correspondiente.

| Imagen | Apellidos y nombres | Código | Carrera | Perfil |
|:---:|:---|:---:|:---|:---|
| <img src="docs/assets/chapter-01/profile_caceres.png" alt="Foto de Albino Caceres" width="120" /> | **Cáceres Pizarro, Albino Florencio** | U201923820 | Ingeniería de Software | Me considero una persona responsable y proactiva que le gusta trabajar en equipo. Además, siempre estoy abierto a ayudar, en lo posible, a cualquier integrante del equipo. Además, busco adaptarme rápidamente a los diversos retos que se presentan en el ciclo. |
| `<img src="docs/assets/chapter-01/[FOTO_INTEGRANTE_2]" alt="Foto de [NOMBRE_INTEGRANTE_2]" width="120" />` | **[APELLIDOS, NOMBRES]** | [CÓDIGO] | Ingeniería de Software | [Describir brevemente su formación, habilidades técnicas, fortalezas personales y aporte al proyecto.] |
| `<img src="docs/assets/chapter-01/[FOTO_INTEGRANTE_3]" alt="Foto de [NOMBRE_INTEGRANTE_3]" width="120" />` | **[APELLIDOS, NOMBRES]** | [CÓDIGO] | Ingeniería de Software | [Describir brevemente su formación, habilidades técnicas, fortalezas personales y aporte al proyecto.] |
| `<img src="docs/assets/chapter-01/[FOTO_INTEGRANTE_4]" alt="Foto de [NOMBRE_INTEGRANTE_4]" width="120" />` | **[APELLIDOS, NOMBRES]** | [CÓDIGO] | Ingeniería de Software | [Describir brevemente su formación, habilidades técnicas, fortalezas personales y aporte al proyecto.] |
| `<img src="docs/assets/chapter-01/[FOTO_INTEGRANTE_5]" alt="Foto de [NOMBRE_INTEGRANTE_5]" width="120" />` | **[APELLIDOS, NOMBRES]** | [CÓDIGO] | Ingeniería de Software | [Describir brevemente su formación, habilidades técnicas, fortalezas personales y aporte al proyecto.] |

---

## 1.2. Solution Profile

Nuestra solución, **MarketGo**, es una plataforma web orientada a la **gestión, conservación y abastecimiento de productos orgánicos**. La solución conecta a administradores de minimarkets y proveedores dentro de un mismo ecosistema digital, permitiendo administrar inventarios, lotes, pedidos, entregas y condiciones de almacenamiento desde una plataforma centralizada.

Para los **administradores de minimarkets**, la plataforma permite controlar el inventario propio, gestionar lotes y fechas de vencimiento, monitorear las condiciones ambientales de almacenamiento, recibir alertas sobre productos en riesgo y gestionar procesos de merma o donación. Asimismo, permite consultar la disponibilidad de productos por lote de proveedores conectados, generar pedidos de abastecimiento y realizar seguimiento de sus estados.

Para los **proveedores**, la plataforma permite publicar productos y lotes disponibles, establecer precios por volumen, gestionar su inventario, atender pedidos provenientes de diferentes minimarkets y realizar el seguimiento de los despachos y entregas.

La solución busca reducir las pérdidas asociadas al deterioro de productos orgánicos y mejorar la coordinación entre compradores y proveedores mediante información centralizada, trazabilidad y flujos de trabajo diferenciados para cada segmento.

### 1.2.1. Antecedentes y problemática

Los productos orgánicos y alimentos frescos presentan una alta sensibilidad a factores como la temperatura, humedad, manipulación y tiempo de almacenamiento. Cuando estas condiciones no son controladas adecuadamente, aumenta el riesgo de deterioro y, como consecuencia, pueden generarse pérdidas económicas, desperdicio de alimentos y disminución de la disponibilidad de productos para los consumidores.

En los minimarkets, uno de los principales desafíos consiste en mantener un control adecuado sobre los productos almacenados, sus lotes y fechas de vencimiento. La ausencia de mecanismos centralizados de seguimiento puede dificultar la identificación temprana de productos en riesgo y provocar que estos sean detectados cuando ya no pueden comercializarse.

A esta problemática se suma la necesidad de mantener condiciones apropiadas de conservación. El monitoreo manual o fragmentado de variables como temperatura y humedad limita la capacidad de los responsables del establecimiento para identificar oportunamente situaciones anómalas que puedan afectar determinados productos.

Por otro lado, el abastecimiento representa un segundo desafío. Los administradores de minimarkets necesitan conocer qué productos y lotes se encuentran disponibles en los proveedores para realizar pedidos oportunamente, mientras que los proveedores necesitan gestionar múltiples pedidos provenientes de diferentes clientes sin perder trazabilidad sobre el estado de cada operación.

Esta situación genera una fragmentación de información entre inventarios, pedidos, entregas e incidencias. La utilización de herramientas no especializadas puede dificultar la coordinación entre ambas partes y aumentar el riesgo de errores, retrasos y pérdidas de productos.

Ante este escenario, se propone una plataforma digital que centralice la información de inventarios, lotes, conservación y abastecimiento, manteniendo separados los procesos de negocio de los administradores de minimarkets y proveedores, pero conectándolos mediante el flujo de pedidos.

**Técnica "The 5W's y 2H's" aplicada al problema:**

| The 5W's y 2H's | Pregunta | Descripción |
|:---|:---|:---|
| **Who** | ¿Quiénes están involucrados? | Administradores de minimarkets responsables de la comercialización y abastecimiento de productos orgánicos, y proveedores encargados de ofrecer, almacenar y distribuir dichos productos. |
| **What** | ¿Cuál es el problema? | Dificultad para gestionar de manera integrada el inventario, conservación, lotes, vencimientos y abastecimiento de productos orgánicos, generando riesgo de pérdidas y desabastecimiento. |
| **Where** | ¿Dónde ocurre? | Principalmente en los procesos de almacenamiento y comercialización de productos orgánicos en minimarkets, así como en la gestión de inventarios, pedidos y entregas de los proveedores. |
| **When** | ¿Cuándo sucede? | Durante el almacenamiento, seguimiento de lotes, control de fechas de vencimiento y procesos de abastecimiento, despacho y entrega de productos. |
| **Why** | ¿Por qué sucede? | Debido a la fragmentación de la información, utilización de procesos manuales y ausencia de una plataforma especializada que conecte inventario, conservación y abastecimiento. |
| **How** | ¿Cómo se manifiesta? | Mediante dificultades para identificar productos en riesgo, controlar lotes y vencimientos, conocer disponibilidad de proveedores, realizar pedidos y dar seguimiento a entregas e incidencias. |
| **How Much** | ¿Cuánto impacto tiene? | El problema puede traducirse en pérdidas económicas por productos deteriorados o vencidos, desperdicio de alimentos, interrupciones en el abastecimiento y mayores costos operativos. |

---

### 1.2.2. Lean UX Process

#### 1.2.2.1. Lean UX Problem Statements

Los administradores de minimarkets que comercializan productos orgánicos necesitan mantener un control constante sobre sus inventarios, lotes, fechas de vencimiento y condiciones de almacenamiento. Sin embargo, la información puede encontrarse fragmentada entre diferentes registros y herramientas, dificultando la identificación temprana de productos en riesgo.

La ausencia de monitoreo integrado de las condiciones ambientales también limita la capacidad de los responsables para reaccionar oportunamente ante variaciones de temperatura o humedad que puedan afectar la conservación de los productos.

Paralelamente, los administradores de minimarkets necesitan mantener una comunicación eficiente con sus proveedores para conocer la disponibilidad de productos y realizar pedidos de abastecimiento. Los proveedores, por su parte, necesitan administrar pedidos de múltiples minimarkets y mantener la trazabilidad de sus despachos.

Como consecuencia, pueden producirse pérdidas por deterioro, vencimiento, errores en pedidos, retrasos en entregas y situaciones de desabastecimiento.

Ante esto nos surge la siguiente pregunta:

**¿Cómo podría una plataforma web centralizar la gestión de inventarios, conservación y abastecimiento de productos orgánicos para reducir pérdidas y mejorar la coordinación entre administradores de minimarkets y proveedores?**

1. **Domain:** Gestión, conservación y abastecimiento de productos orgánicos.

2. **Customer Segments:** Administradores de minimarkets y proveedores de productos orgánicos.

3. **Pain Points:** Pérdidas por deterioro o vencimiento, falta de visibilidad sobre las condiciones de almacenamiento, dificultades para controlar lotes y problemas de coordinación durante el abastecimiento.

4. **Gap:** Falta de una plataforma especializada que integre inventario, lotes, conservación y abastecimiento entre minimarkets y proveedores.

5. **Vision/Strategy:** Centralizar digitalmente la información operativa y proporcionar herramientas que permitan identificar riesgos, gestionar inventarios y facilitar el abastecimiento.

6. **Initial Segment:** Administradores de minimarkets y proveedores de productos orgánicos que requieran mejorar el control de inventarios, conservación y coordinación de abastecimiento.

---

#### 1.2.2.2. Lean UX Assumptions

**Business Assumptions:**

1. Se considera que los administradores de minimarkets necesitan mejorar el control de sus productos orgánicos para reducir pérdidas asociadas al deterioro y vencimiento.

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

1. Los administradores de minimarkets necesitan visualizar rápidamente el estado de su inventario y los productos próximos a vencer.

2. Los administradores de minimarkets valoran recibir alertas cuando las condiciones de almacenamiento puedan afectar determinados productos.

3. Los administradores de minimarkets necesitan consultar la disponibilidad de productos y lotes de proveedores conectados.

4. Los proveedores necesitan visualizar y gestionar los pedidos recibidos de diferentes minimarkets desde un único sistema.

5. Los proveedores requieren controlar la disponibilidad de sus lotes y establecer precios de acuerdo con el volumen solicitado.

6. Ambos segmentos necesitan consultar el estado de un pedido y comunicarse respecto a incidencias asociadas a la operación.

**User Outcome Assumptions**

1. Los administradores de minimarkets tendrán mayor confianza en la información de su inventario al disponer de un registro centralizado de productos, lotes y vencimientos.

2. Los administradores de minimarkets podrán identificar oportunamente condiciones ambientales anómalas que puedan representar un riesgo para los productos.

3. Los administradores de minimarkets podrán encontrar productos disponibles en proveedores conectados sin depender de múltiples canales de comunicación.

4. Los proveedores podrán administrar sus pedidos de manera más organizada y mantener trazabilidad sobre cada operación.

5. Los usuarios experimentarán una reducción de la incertidumbre respecto al estado de los pedidos y entregas.

6. Los administradores de ambos segmentos podrán tomar decisiones operativas con mayor rapidez al contar con información centralizada y actualizada.

---

#### 1.2.2.3. Lean UX Hypothesis Statements

**Hypothesis 1**

Creemos que al centralizar la gestión de inventarios, lotes y fechas de vencimiento de los minimarkets, facilitaremos la identificación de productos próximos a vencer. Lo sabremos cuando los administradores puedan identificar los productos críticos desde el dashboard sin necesidad de consultar diferentes registros.

**Hypothesis 2**

Creemos que al implementar un sistema de monitoreo de temperatura y humedad, acompañado de alertas basadas en los requisitos de conservación de cada producto, mejoraremos la capacidad de los administradores para detectar condiciones de riesgo. Lo sabremos cuando puedan identificar y atender oportunamente las alertas generadas.

**Hypothesis 3**

Creemos que al conectar la disponibilidad de productos y lotes de los proveedores con los minimarkets, reduciremos el tiempo necesario para encontrar productos disponibles para abastecimiento. Lo sabremos cuando los administradores puedan localizar y seleccionar productos de proveedores conectados desde la plataforma.

**Hypothesis 4**

Creemos que al centralizar el ciclo de vida de los pedidos, reduciremos la incertidumbre sobre el estado de las operaciones de abastecimiento. Lo sabremos cuando administradores de minimarkets y proveedores puedan consultar el estado actualizado de cada pedido sin utilizar canales externos de comunicación.

**Hypothesis 5**

Creemos que al proporcionar dashboards diferenciados para administradores de minimarkets y proveedores, mejoraremos la experiencia de cada segmento al mostrar únicamente las funcionalidades y métricas relevantes para su operación. Lo sabremos cuando los usuarios puedan completar sus principales tareas sin acceder a funcionalidades que no correspondan a su segmento.

---

#### 1.2.2.4. Lean UX Canvas

<table>
  <tr>
    <td valign="top">
      <strong>Business problem</strong>
      <br><br>
      Los administradores de minimarkets y proveedores de productos orgánicos gestionan inventarios, lotes, conservación y abastecimiento mediante procesos que pueden encontrarse fragmentados.
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
      - Dashboard diferenciado para administradores de minimarkets y proveedores
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
      Si los administradores de minimarkets y proveedores perciben suficiente valor en una plataforma integrada de gestión de inventario, conservación y abastecimiento como para incorporarla a sus procesos operativos.
    </td>
    <td valign="top">
      <strong>What’s the least amount of work we need to do to learn the next most important thing?</strong>
      <br><br>
      Realizar entrevistas con administradores de minimarkets y proveedores y validar mediante un prototipo de baja fidelidad los flujos principales de inventario, alertas, consulta de disponibilidad y gestión de pedidos.
    </td>
  </tr>
</table>

---

## 1.3. Segmentos Objetivos

La solución está dirigida a **dos segmentos objetivos principales** que participan directamente en la cadena de abastecimiento de productos orgánicos: **administradores de minimarkets y proveedores**.

Estos segmentos representan dos tipos de organizaciones con necesidades de negocio diferentes. Por ello, la plataforma utiliza una infraestructura tecnológica compartida, pero ofrece dashboards, funcionalidades y permisos específicos para cada segmento.

Los roles operativos que puedan existir dentro de cada empresa forman parte de la estructura interna de cada segmento y no constituyen segmentos objetivos independientes.

### 1.3.1. Administradores de Minimarkets

| Dimensión | Detalle del perfil |
|---|---|
| **Perfil Demográfico** | Propietarios, administradores o responsables de pequeños y medianos minimarkets dedicados a la comercialización de productos orgánicos y alimentos frescos. Son responsables de supervisar las operaciones comerciales y tomar decisiones relacionadas con inventario, conservación y abastecimiento. |
| **Perfil Geográfico** | Negocios ubicados principalmente en zonas urbanas con demanda de productos orgánicos y necesidad de mantener un abastecimiento constante. El segmento inicial puede concentrarse en Lima Metropolitana. |
| **Perfil Psicográfico** | Personas orientadas a mantener la calidad de sus productos, reducir pérdidas y asegurar la disponibilidad constante de mercadería. Valoran soluciones sencillas que permitan controlar las operaciones del negocio y tomar decisiones basadas en información actualizada. |
| **Puntos de Dolor** | Pérdidas ocasionadas por deterioro o vencimiento de productos, dificultad para controlar lotes y fechas de vencimiento, falta de visibilidad sobre las condiciones de almacenamiento, desabastecimiento y dificultad para encontrar proveedores disponibles. |
| **Uso de Tecnología** | Utilizan herramientas digitales para administrar ventas, inventarios y comunicación con proveedores, aunque pueden depender de hojas de cálculo, aplicaciones de mensajería y sistemas independientes que no integran toda la información operativa. |

### 1.3.2. Proveedores

| Dimensión | Detalle del perfil |
|---|---|
| **Perfil Demográfico** | Empresas, productores, distribuidores o comerciantes mayoristas de productos orgánicos que abastecen a minimarkets. Sus representantes son responsables de gestionar el catálogo, inventario, lotes, pedidos y despachos. |
| **Perfil Geográfico** | Proveedores ubicados en zonas productoras, centros de distribución o áreas comerciales que atienden a minimarkets y otros negocios comercializadores de productos orgánicos. |
| **Perfil Psicográfico** | Negocios orientados a mantener una rotación eficiente de sus productos, atender pedidos oportunamente y establecer relaciones comerciales duraderas con sus clientes. Valoran la trazabilidad, organización y visibilidad de sus operaciones comerciales. |
| **Puntos de Dolor** | Dificultad para administrar pedidos de múltiples minimarkets, falta de visibilidad sobre el estado de las operaciones, gestión fragmentada de inventarios y lotes, y dificultades para coordinar despachos y entregas. |
| **Uso de Tecnología** | Utilizan herramientas digitales, hojas de cálculo y aplicaciones de comunicación para gestionar inventarios, clientes y pedidos, pero pueden carecer de una plataforma especializada que conecte directamente su disponibilidad de productos con los minimarkets. |

<!-- AUTO-DOCS:END -->
