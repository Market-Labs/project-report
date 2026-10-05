# Capítulo III: Requirements Specification

## 3.1. User Stories.

### TO-BE Scenario Mapping

#### Administradores de Minimarkets

| Fase | Doing (Qué hace) | Thinking (Qué piensa) | Feeling (Qué siente) |
|------|------------------|-----------------------|----------------------|
| Consulta y revisión de información | Consulta el dashboard común para revisar el inventario, productos, lotes, fechas de vencimiento, condiciones de conservación, pedidos y órdenes de envío del minimarket. | “Necesito encontrar rápidamente la información de mis productos y conocer cuáles requieren atención.” | Organizado y con mayor sensación de control. |
| Gestión y abastecimiento | Identifica necesidades de abastecimiento, consulta los productos ofrecidos por los proveedores y genera pedidos indicando los productos y cantidades requeridas. | “Necesito solicitar los productos adecuados para mantener abastecido el minimarket.” | Atento y enfocado en mantener la disponibilidad de productos. |
| Toma de decisión | Consulta las órdenes de envío generadas por los proveedores y decide aceptarlas o rechazarlas después de revisar los productos y cantidades enviados. | “Necesito verificar que los productos recibidos correspondan con lo solicitado antes de incorporarlos al inventario.” | Responsable y seguro al contar con información centralizada. |
| Seguimiento y control | Consulta el estado de sus pedidos y órdenes de envío. Cuando acepta una orden de envío, los productos recibidos se incorporan automáticamente al inventario del minimarket. | “Necesito conocer cómo avanzan mis pedidos y asegurar que solo los productos recibidos ingresen al inventario.” | Vigilante, con mayor sensación de control y seguridad. |

#### Proveedores de Productos Orgánicos

| Fase | Doing (Qué hace) | Thinking (Qué piensa) | Feeling (Qué siente) |
|------|------------------|-----------------------|----------------------|
| Consulta y revisión de información | Consulta el dashboard común para revisar los productos que ofrece, los pedidos recibidos de los minimarkets y las órdenes de envío relacionadas con sus operaciones. | “Necesito conocer qué productos solicitan los minimarkets y revisar rápidamente mis operaciones pendientes.” | Organizado y con mayor claridad sobre sus operaciones. |
| Gestión de pedidos | Consulta los pedidos recibidos de los minimarkets y decide aceptarlos o rechazarlos según su disponibilidad de productos. | “Necesito verificar si puedo atender correctamente los productos y cantidades solicitadas.” | Atento y responsable al evaluar las solicitudes recibidas. |
| Gestión de órdenes de envío | Para los pedidos aceptados, genera una orden de envío indicando los productos, cantidades y demás información correspondiente al despacho. | “Necesito registrar correctamente lo que voy a enviar para que el minimarket pueda verificarlo al recibirlo.” | Enfocado y seguro al mantener trazabilidad del envío. |
| Seguimiento y control | Consulta el estado de las órdenes de envío generadas y verifica si fueron aceptadas o rechazadas por los administradores de los minimarkets. | “Necesito saber si los productos enviados fueron aceptados y mantener un registro de mis operaciones.” | Tranquilo y con mayor sensación de control y trazabilidad. |

### Epics

| EPIC ID | Titulo | Descripcion |
|--------|--------|-------------|
| EP-01 | Gestión de inventario y ventas | Permite consultar y registrar stock, visualizar lotes y vencimientos, registrar mermas y ventas, y consultar los movimientos correspondientes al usuario. |
| EP-02 | Control de lotes y vencimientos | Permite identificar el lote y la fecha de vencimiento de los productos registrados en inventario. |
| EP-03 | Conservación y alertas | Permite visualizar registros de temperatura y humedad y consultar alertas relevantes para el minimarket o proveedor. |
| EP-04 | Abastecimiento | Permite crear solicitudes con varios productos, responderlas, generar órdenes de envío y aceptar o rechazar su recepción. |
| EP-05 | Proveedores y productos | Permite consultar proveedores o clientes según el rol y administrar los productos del catálogo. |
| EP-06 | Identidad y acceso | Permite iniciar sesión, crear usuarios de la propia organización y adaptar la navegación y las acciones al rol autenticado. |
| EP-07 | Dashboard, analítica y reportes | Permite consultar indicadores por rol, visualizar reportes operativos y exportarlos en PDF o XLSX. |

### User Stories

| US ID | Título | Descripción | Criterio de Aceptación | Relacionado con (EPIC ID) |
|------|--------|-------------|------------------------|--------------------------|
| US 001 | Registrar stock | **Como** usuario autorizado,<br>**Quiero** registrar existencias de un producto,<br>**Para** mantener actualizado mi inventario. | El formulario permite seleccionar un producto registrado e ingresar lote, vencimiento, cantidad y stock mínimo. Los campos inválidos impiden guardar. | EP-01 / EP-02 |
| US 002 | Visualizar inventario | **Como** usuario autenticado,<br>**Quiero** consultar mi inventario,<br>**Para** conocer productos, cantidades y estados. | La tabla muestra únicamente el inventario correspondiente a mi organización, con producto, lote, vencimiento, stock y estado. | EP-01 |
| US 003 | Buscar en inventario | **Como** usuario autenticado,<br>**Quiero** buscar registros visibles en inventario,<br>**Para** encontrarlos rápidamente. | La búsqueda filtra los registros mostrados y presenta un estado vacío cuando no hay coincidencias. | EP-01 |
| US 004 | Filtrar inventario | **Como** usuario autenticado,<br>**Quiero** filtrar registros de inventario,<br>**Para** identificar los productos que requieren atención. | Los filtros disponibles modifican la tabla sin mostrar registros de otra organización. | EP-01 / EP-02 |
| US 005 | Actualizar inventario | **Como** usuario autorizado,<br>**Quiero** actualizar las existencias de mi organización,<br>**Para** reflejar los cambios de stock. | Los cambios permitidos se guardan y se muestran en la tabla; no es posible modificar el inventario ajeno. | EP-01 |
| US 006 | Registrar lote al ingresar stock | **Como** usuario autorizado,<br>**Quiero** indicar un código de lote al registrar stock,<br>**Para** identificar la procedencia del registro. | El código de lote queda asociado al registro de inventario creado. | EP-02 |
| US 007 | Consultar lote | **Como** usuario autenticado,<br>**Quiero** ver el lote de cada registro de inventario,<br>**Para** reconocer las existencias asociadas. | El lote aparece en el inventario y en los reportes que incluyen ese dato. | EP-02 |
| US 008 | Consultar vencimiento | **Como** usuario autenticado,<br>**Quiero** consultar la fecha de vencimiento de mis existencias,<br>**Para** priorizar su revisión. | La fecha se muestra junto al producto y lote correspondiente. | EP-02 |
| US 009 | Consultar alertas de vencimiento | **Como** administrador de minimarket,<br>**Quiero** revisar alertas relacionadas con productos en riesgo,<br>**Para** atenderlos oportunamente. | El apartado de Alertas muestra los registros disponibles y permite consultar su estado. | EP-02 / EP-03 |
| US 010 | Consultar condiciones de conservación | **Como** usuario autenticado,<br>**Quiero** consultar registros de conservación de mi organización,<br>**Para** conocer las condiciones de almacenamiento. | La vista muestra los registros disponibles o un estado vacío cuando no existen datos. | EP-03 |
| US 011 | Visualizar temperatura y humedad | **Como** usuario autenticado,<br>**Quiero** visualizar temperatura y humedad,<br>**Para** reconocer condiciones normales o de riesgo. | Cada registro presenta sus valores, fecha, zona y estado. | EP-03 |
| US 012 | Consultar alertas de conservación | **Como** usuario autenticado,<br>**Quiero** revisar las alertas de conservación disponibles,<br>**Para** identificar situaciones que requieren atención. | Desde Conservación puedo acceder a Alertas y consultar los registros correspondientes a mi rol. | EP-03 |
| US 013 | Registrar merma | **Como** usuario autorizado,<br>**Quiero** registrar una merma de mi inventario,<br>**Para** conservar el historial de pérdidas. | El formulario solicita producto, cantidad y motivo. No permite registrar una cantidad superior al stock disponible. | EP-01 / EP-07 |
| US 014 | Registrar venta | **Como** administrador de minimarket,<br>**Quiero** registrar una venta con uno o varios productos,<br>**Para** consultar la operación y mantener actualizado el stock. | El formulario permite seleccionar productos registrados, cantidades y descuento; calcula el total y valida la disponibilidad. | EP-01 / EP-07 |
| US 015 | Consultar productos de proveedores | **Como** administrador de minimarket,<br>**Quiero** consultar el catálogo de productos,<br>**Para** identificar opciones de abastecimiento. | Las tarjetas muestran nombre, categoría, precio, disponibilidad, identificador y proveedor. | EP-05 |
| US 016 | Registrar producto ofrecido | **Como** proveedor,<br>**Quiero** agregar productos a mi catálogo,<br>**Para** ofrecerlos a los minimarkets. | El formulario valida los datos obligatorios y muestra el producto registrado con un identificador según su categoría. | EP-05 |
| US 017 | Consultar productos ofrecidos | **Como** proveedor,<br>**Quiero** consultar mis productos,<br>**Para** revisar su información y disponibilidad. | La vista muestra los productos asociados al proveedor autenticado. | EP-05 |
| US 018 | Crear solicitud de abastecimiento | **Como** administrador de minimarket,<br>**Quiero** solicitar varios productos registrados a un proveedor,<br>**Para** abastecer mi negocio mediante una sola solicitud. | El formulario permite seleccionar proveedor, productos y cantidades; la solicitud creada contiene todos sus ítems. | EP-04 |
| US 019 | Consultar solicitudes | **Como** administrador o proveedor,<br>**Quiero** consultar solicitudes y abrir su detalle,<br>**Para** revisar productos, cantidades y estado. | El administrador ve las solicitudes de su minimarket; el proveedor ve las dirigidas a él. «Ver detalles» presenta todos los ítems. | EP-04 / EP-06 |
| US 020 | Aceptar o rechazar solicitud | **Como** proveedor,<br>**Quiero** responder a una solicitud recibida,<br>**Para** indicar si puedo atenderla. | El proveedor puede aceptar o rechazar una solicitud pendiente dirigida a él, sin modificar los productos ni cantidades solicitados. | EP-04 |
| US 021 | Generar orden de envío | **Como** proveedor,<br>**Quiero** generar una orden de envío a partir de una solicitud aceptada,<br>**Para** registrar los productos que enviaré. | La acción está disponible para solicitudes aceptadas y crea una orden vinculada con estado pendiente de recepción. | EP-04 |
| US 022 | Consultar órdenes de envío | **Como** administrador o proveedor,<br>**Quiero** consultar las órdenes y abrir su detalle,<br>**Para** revisar todos los productos enviados. | El proveedor ve sus órdenes; el administrador ve las destinadas a su minimarket. «Ver detalles» muestra todos los ítems. | EP-04 / EP-06 |
| US 023 | Aceptar recepción | **Como** administrador de minimarket,<br>**Quiero** aceptar una orden pendiente,<br>**Para** incorporar al inventario los productos recibidos. | La acción marca la orden como recibida y actualiza el inventario. Una orden ya procesada no puede recibirse nuevamente. | EP-01 / EP-04 |
| US 024 | Rechazar recepción | **Como** administrador de minimarket,<br>**Quiero** rechazar una orden pendiente,<br>**Para** evitar incorporar productos no aceptados. | El formulario solicita un motivo; al rechazar la orden no se incrementa el inventario. | EP-04 |
| US 025 | Consultar seguimiento de abastecimiento | **Como** usuario autenticado,<br>**Quiero** consultar el estado de mis solicitudes y órdenes,<br>**Para** seguir las operaciones de abastecimiento. | Las listas y detalles muestran identificador, participantes, productos y estado correspondientes al usuario. | EP-04 / EP-07 |
| US 026 | Crear usuarios de mi organización | **Como** administrador o proveedor autorizado,<br>**Quiero** crear usuarios para mi organización,<br>**Para** delegar el acceso a MarketGo. | Ambos roles disponen de «Nuevo usuario». El formulario solicita nombre, correo y contraseña y muestra el rol que recibirá la nueva cuenta. | EP-06 |
| US 027 | Iniciar sesión | **Como** usuario,<br>**Quiero** iniciar sesión con correo y contraseña,<br>**Para** acceder a las pantallas de mi rol. | Las credenciales válidas abren la aplicación; las inválidas muestran un error sin conceder acceso. | EP-06 |
| US 028 | Visualizar roles y permisos | **Como** usuario autorizado,<br>**Quiero** consultar los usuarios y roles de mi organización,<br>**Para** conocer quiénes tienen acceso. | La tabla muestra únicamente usuarios de la organización. El formulario de creación no permite asignar arbitrariamente otro rol. | EP-06 |
| US 029 | Mostrar acciones según el rol | **Como** usuario autenticado,<br>**Quiero** ver únicamente las acciones que me corresponden,<br>**Para** evitar operaciones no autorizadas. | El administrador crea solicitudes y revisa recepciones; el proveedor responde solicitudes y genera envíos. Ninguno edita el contenido de órdenes creadas por la otra parte. | EP-04 / EP-06 |
| US 030 | Consultar dashboard por rol | **Como** usuario autenticado,<br>**Quiero** ver un dashboard común adaptado a mi rol,<br>**Para** revisar mis operaciones. | Ambos roles comparten el layout; el menú, indicadores y datos visibles corresponden a su organización. | EP-07 |
| US 031 | Visualizar y exportar reportes | **Como** usuario autenticado,<br>**Quiero** seleccionar un reporte, previsualizarlo y exportarlo,<br>**Para** analizar mis operaciones fuera de MarketGo. | Al seleccionar Inventario, Abastecimiento, Mermas, Conservación, Proveedores o Ventas se muestra el reporte; desde su vista previa puede exportarse en PDF o XLSX. | EP-07 |
| US 032 | Consultar ventas propias | **Como** usuario autenticado,<br>**Quiero** consultar las ventas correspondientes a mi rol,<br>**Para** revisar mis operaciones comerciales. | El administrador consulta las ventas minoristas del minimarket; el proveedor consulta las operaciones derivadas de sus envíos recibidos. | EP-07 |
| US 033 | Editar o eliminar producto | **Como** usuario autorizado,<br>**Quiero** actualizar precio y descripción o eliminar un producto,<br>**Para** mantener vigente mi catálogo. | La tarjeta del producto muestra las acciones disponibles. El proveedor no puede modificar productos de otro proveedor. | EP-05 |

### Technical Stories

Estas historias corresponden únicamente al **frontend**. No definen ni sustituyen contratos o tareas del backend.

| TS ID | Título | Descripción | Criterios de Aceptación | Relacionado con (EPIC ID) |
|------|--------|-------------|--------------------------|---------------------------|
| TS-FE-001 | Integración de inicio de sesión | Como desarrollador frontend, quiero conectar la pantalla de login con Firebase Authentication para mantener una sesión de usuario. | El login muestra errores controlados, restaura la sesión cuando corresponde y permite cerrarla. | EP-06 |
| TS-FE-002 | Adaptador de datos del frontend | Como desarrollador frontend, quiero consumir los datos de Firestore mediante los adaptadores existentes para conservar la arquitectura por bounded context. | Las vistas obtienen y actualizan los datos mediante stores y adaptadores, sin consultas directas desde los componentes. | EP-01 / EP-04 / EP-05 |
| TS-FE-003 | Navegación por rol | Como desarrollador frontend, quiero adaptar rutas, menú y acciones al usuario autenticado. | El administrador y el proveedor comparten layout, pero ven etiquetas, datos y acciones correspondientes a su rol. | EP-06 |
| TS-FE-004 | Formularios y validación | Como desarrollador frontend, quiero validar los formularios antes de guardar para evitar entradas incompletas o inválidas. | Los formularios muestran campos apropiados, opciones de selección cuando existen datos registrados y mensajes de error comprensibles. | EP-01 / EP-04 / EP-05 / EP-06 |
| TS-FE-005 | Búsqueda e internacionalización | Como desarrollador frontend, quiero que las tablas visibles puedan buscarse y que sus etiquetas cambien entre español e inglés. | La búsqueda filtra los registros mostrados y los textos de las vistas y tablas responden al selector de idioma. | EP-01 / EP-07 |
| TS-FE-006 | Vista previa y exportación de reportes | Como desarrollador frontend, quiero generar la vista del reporte seleccionado y ofrecer exportación PDF/XLSX. | Cada opción actualiza su tabla de resultados; las acciones de exportación corresponden al reporte visible. | EP-07 |
| TS-FE-007 | Compilación para Azure | Como desarrollador frontend, quiero que la aplicación desplegada use el modo Firebase para consultar datos y permitir el inicio de sesión. | La compilación de producción se realiza con `VITE_DATA_SOURCE=firebase` y conserva las rutas del frontend. | EP-06 / EP-07 |

#### Functional Stories

| FS ID | Título | Descripción | Criterios de Aceptación | Relacionado con (EPIC ID) |
|------|--------|-------------|--------------------------|---------------------------|
| FS-001 | Interfaz de solicitudes según rol | Como usuario, quiero que el módulo de Solicitudes muestre las acciones de mi rol. | El administrador puede crear y consultar solicitudes; el proveedor puede consultar las recibidas y aceptarlas o rechazarlas sin editar sus ítems. | EP-04 / EP-06 |
| FS-002 | Interfaz de envíos según rol | Como usuario, quiero que el módulo de envíos muestre las acciones de mi rol. | El proveedor puede generar y consultar órdenes; el administrador puede consultar las recibidas y aceptar o rechazar su recepción sin editar sus ítems. | EP-04 / EP-06 |
| FS-003 | Creación de usuarios por organización | Como usuario autorizado, quiero disponer de la opción «Nuevo usuario» en mi apartado de Usuarios y roles. | Tanto administrador como proveedor pueden abrir el formulario; la lista de usuarios y el rol mostrado corresponden a su organización. | EP-06 |

## 3.2. Impact Mapping.

El Impact Mapping relaciona los objetivos de MarketGo con los comportamientos que facilita el frontend. Las metas son objetivos del producto; la interfaz por sí sola no demuestra que ya se hayan alcanzado.

<p align="center">
  <img src="assets/chapter-03/impact-mapping.png" alt="Impact Mapping de MarketGo" width="100%">
</p>
<p align="center"><em>Figura: Impact Mapping de MarketGo.</em></p>

**Business Goal 1 – Reducción de mermas (Persona: Russell Estrada, administrador de minimarket orgánico)**

| Business Goal (SMART) | Persona | Impact | Deliverable frontend | User Stories |
|---|---|---|---|---|
| Reducir en 30% las mermas por vencimiento y deterioro durante los primeros 6 meses desde el lanzamiento. | Russell Estrada | Consulta existencias, lotes y vencimientos sin depender de una revisión manual completa. | Inventario con búsqueda, filtros y datos de lote y vencimiento. | US001–US008 |
| | | Identifica condiciones y avisos que requieren atención. | Vistas de Conservación y Alertas. | US009–US012 |
| | | Registra pérdidas y ventas y compara sus resultados. | Formularios de mermas y ventas; reportes de Inventario, Mermas, Conservación y Ventas. | US013, US014, US031 |

**Business Goal 2 – Agilización del abastecimiento (Personas: Russell Estrada y Marco Antonio Ríos, proveedor B2B)**

| Business Goal (SMART) | Persona | Impact | Deliverable frontend | User Stories |
|---|---|---|---|---|
| Reducir de 24 h a menos de 4 h el tiempo promedio entre la creación de una solicitud y la generación de su orden de envío, en el 80% de las solicitudes gestionadas durante el primer semestre. | Russell Estrada | Consulta productos y crea solicitudes estructuradas con varios ítems. | Catálogo y formulario de Solicitudes. | US015, US018, US019 |
| | | Revisa el envío y confirma o rechaza su recepción. | Detalle de órdenes y acciones de recepción. | US022–US024 |
| | Marco Antonio Ríos | Mantiene visible su catálogo y responde las solicitudes recibidas. | Productos, Solicitudes y generación de órdenes de envío. | US016, US017, US020, US021, US033 |
| | | Consulta sus operaciones sin acceder a información de otras organizaciones. | Dashboard, ventas, reportes y navegación por rol. | US025–US032 |

## 3.3. Product Backlog.

| Orden | User Story ID | Título | Descripción | Story Points |
|------|---------------|--------|-------------|--------------|
| 1 | US-001 | Registrar stock | Formulario para registrar existencias, lote y vencimiento. | 5 |
| 2 | US-002 | Visualizar inventario | Tabla del inventario correspondiente al usuario. | 5 |
| 3 | US-003 | Buscar en inventario | Búsqueda entre los registros visibles. | 3 |
| 4 | US-004 | Filtrar inventario | Filtros sobre los registros del inventario. | 3 |
| 5 | US-005 | Actualizar inventario | Actualización permitida de existencias propias. | 5 |
| 6 | US-006 | Registrar lote al ingresar stock | Código de lote asociado al registro de inventario. | 3 |
| 7 | US-007 | Consultar lote | Visualización del lote de cada registro. | 3 |
| 8 | US-008 | Consultar vencimiento | Visualización de fechas de vencimiento. | 3 |
| 9 | US-009 | Consultar alertas de vencimiento | Consulta de los avisos disponibles. | 3 |
| 10 | US-010 | Consultar condiciones de conservación | Vista de registros de conservación. | 3 |
| 11 | US-011 | Visualizar temperatura y humedad | Valores y estados por registro. | 3 |
| 12 | US-012 | Consultar alertas de conservación | Acceso a los avisos de conservación. | 3 |
| 13 | US-013 | Registrar merma | Formulario de merma con validación de cantidad. | 5 |
| 14 | US-014 | Registrar venta | Venta de varios productos con total y validación de stock. | 5 |
| 15 | US-015 | Consultar productos de proveedores | Catálogo con datos del producto y proveedor. | 3 |
| 16 | US-016 | Registrar producto ofrecido | Formulario para agregar productos al catálogo. | 5 |
| 17 | US-017 | Consultar productos ofrecidos | Vista de productos asociados al proveedor. | 3 |
| 18 | US-018 | Crear solicitud de abastecimiento | Solicitud con proveedor y varios productos. | 5 |
| 19 | US-019 | Consultar solicitudes | Tabla y detalle completo de solicitudes. | 3 |
| 20 | US-020 | Aceptar o rechazar solicitud | Acciones de respuesta del proveedor. | 3 |
| 21 | US-021 | Generar orden de envío | Orden vinculada a una solicitud aceptada. | 5 |
| 22 | US-022 | Consultar órdenes de envío | Tabla y detalle completo de órdenes. | 3 |
| 23 | US-023 | Aceptar recepción | Confirmación de recepción y actualización del inventario. | 5 |
| 24 | US-024 | Rechazar recepción | Rechazo con motivo, sin incorporar productos. | 3 |
| 25 | US-025 | Consultar seguimiento de abastecimiento | Estados y detalles de solicitudes y órdenes. | 3 |
| 26 | US-026 | Crear usuarios de mi organización | Formulario de nuevo usuario para ambos roles. | 5 |
| 27 | US-027 | Iniciar sesión | Login con correo y contraseña. | 3 |
| 28 | US-028 | Visualizar roles y permisos | Tabla de usuarios y rol de la organización. | 3 |
| 29 | US-029 | Mostrar acciones según el rol | Navegación y acciones correspondientes al usuario. | 5 |
| 30 | US-030 | Consultar dashboard por rol | Dashboard común con datos y accesos por rol. | 5 |
| 31 | US-031 | Visualizar y exportar reportes | Vista previa y exportación PDF/XLSX. | 5 |
| 32 | US-032 | Consultar ventas propias | Vista de ventas del minimarket o proveedor. | 3 |
| 33 | US-033 | Editar o eliminar producto | Acciones de mantenimiento del catálogo. | 5 |
| 34 | TS-FE-001 | Integración de inicio de sesión | Sesión y login desde el frontend. | 3 |
| 35 | TS-FE-002 | Adaptador de datos del frontend | Integración de datos mediante stores y adaptadores existentes. | 5 |
| 36 | TS-FE-003 | Navegación por rol | Rutas, menú y acciones por rol. | 3 |
| 37 | TS-FE-004 | Formularios y validación | Campos de selección, validaciones y mensajes. | 3 |
| 38 | TS-FE-005 | Búsqueda e internacionalización | Búsqueda en tablas y cambio español/inglés. | 3 |
| 39 | TS-FE-006 | Vista previa y exportación de reportes | Reportes seleccionables y exportables. | 5 |
| 40 | TS-FE-007 | Compilación para Azure | Build del frontend en modo Firebase. | 2 |
| 41 | FS-001 | Interfaz de solicitudes según rol | Acciones distintas para administrador y proveedor. | 3 |
| 42 | FS-002 | Interfaz de envíos según rol | Generación de envíos y revisión de recepción. | 3 |
| 43 | FS-003 | Creación de usuarios por organización | Formulario disponible para los dos roles. | 3 |

**Enlace directo al tablero:** 
**Tablero Sprint 1: Trello**
[Tablero Sprint 1 en Trello](https://trello.com/b/AyBgUYcT/springbacklog1)

<div align="center">
  <img src="assets/chapter-03/tableroTrello.png" alt="Evidence Product Backlog" width="90%">
  <p><em>Figura: Captura del Product Backlog en la herramienta de gestión del proyecto.</em></p>
</div>

