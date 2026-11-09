# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management.

En esta sección se describen las decisiones, convenciones y principios adoptados por el equipo de **Market-Labs** para garantizar la coherencia, trazabilidad y control de versiones durante el ciclo de vida del desarrollo de la solución **MarketGo**. Se establecen los lineamientos para la configuración del entorno de desarrollo, gestión del código fuente, convenciones de estilo y configuración de despliegue orientada a la nube.

### 5.1.1. Software Development Environment Configuration.

Se especifican los productos de software utilizados durante el ciclo de vida del proyecto, organizados por disciplinas técnicas para asegurar la estandarización del entorno entre los desarrolladores de MarketGo.

#### Project Management
* **Jira:** Empleado para la organización visual del flujo de trabajo diario y la priorización rápida de tareas durante el desarrollo de los módulos de inventario y pedidos (Atlassian, s. f.).
    * **Ruta:** [https://trello.com/invite/b/6aaf23b3497a9f7b08a946ed/ATTIc6df49d5561e92016f5670f633077371DA4CB5DA/marketgo](https://trello.com/invite/b/6aaf23b3497a9f7b08a946ed/ATTIc6df49d5561e92016f5670f633077371DA4CB5DA/marketgo)
 
#### Product UX/UI Design
1.  **LucidChart:** Pizarra colaborativa usada para el Design-Level EventStorming de MarketGo y la identificación de eventos de inventario y abastecimiento.
2.  **Figma:** Herramienta principal para el diseño de la landing page y la plataforma web de gestión, incluyendo el diseño del sistema de diseño (Design System).
3.  **Structurizr:** Utilizado para el modelado de la arquitectura de software mediante diagramas C4 y diagramas de base de datos relacional.

#### Software Development
1.  **GitHub:** Hosting de repositorios bajo la organización Market-Labs. Implementación de GitFlow para separar las funcionalidades de inventario, compras y reportes (GitHub, s. f.).
2.  **WebStorm:** IDE especializado para el desarrollo del Frontend de MarketGo, optimizando la codificación con Vue.js y la gestión de estilos.
3.  **JetBrains Rider:** IDE principal para el desarrollo del Backend robusto basado en .NET/C#, facilitando la integración con servicios de base de datos y lógica de negocio.
4.  **Vue.js Framework:** Framework de JavaScript elegido para construir la interfaz de la aplicación web de MarketGo (Vue.js, s. f.-a).
5.  **ASP.NET Core / C# sobre .NET 10:** Tecnología de backend para garantizar la escalabilidad, seguridad transaccional en las órdenes de pedido y alto rendimiento.

#### Software Testing
* **Lenguaje Gherkin:** Utilizado para definir los criterios de aceptación en formato Given-When-Then de pedidos e inventario (Cucumber, s. f.).

#### Software Documentation
* **Swagger / OpenAPI:** Generación de documentación interactiva para que el equipo de Frontend pueda consumir los servicios de pedidos y proveedores de forma eficiente.

---
### 5.1.2. Source Code Management.

Se establecen los repositorios oficiales de la solución MarketGo para garantizar la integridad del código fuente.

#### Repositorios del Proyecto
<table>
  <thead>
    <tr>
      <th>Producto</th>
      <th>URL del Repositorio</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Organización Market-Labs</td>
      <td><a href="https://github.com/Market-Labs">https://github.com/Market-Labs</a></td>
    </tr>
    <tr>
      <td>Landing Page</td>
      <td><a href="https://github.com/Market-Labs/landign-page">https://github.com/Market-Labs/landign-page</a></td>
    </tr>
    <tr>
      <td>Frontend Web Application</td>
      <td><a href="https://github.com/Market-Labs/front-end">https://github.com/Market-Labs/front-end</a></td>
    </tr>
    <tr>
      <td>Backend Web Services</td>
      <td><a href="https://github.com/Market-Labs/backend.git">https://github.com/Market-Labs/backend.git</a></td>
    </tr>
  </tbody>
</table>

#### GitFlow Workflow and Collaboration Strategy

Para asegurar una colaboración organizada, evitar conflictos en el código y mantener una integración continua clara, el equipo de **MarketLab** aplica **GitFlow** como flujo de trabajo de ramificación para el desarrollo de la landing page de **MarketGo**.

La estrategia de colaboración se define de la siguiente manera:

- **main:** Rama que contiene la versión estable y lista para producción de la landing page. Solo recibe integraciones finales desde `develop` cuando los cambios han sido revisados, probados y aprobados.

- **develop:** Rama principal de integración. En esta rama se unifican las funcionalidades terminadas antes de ser promovidas a `main`.

- **feature/<section>:** Ramas temporales creadas a partir de `develop` para aislar el desarrollo de cada sección o mejora de la landing page.  
  Ejemplos:
  - `feature/home-section`
  - `feature/product-information-section`
  - `feature/video-section`
  - `feature/pricing-section`
  - `feature/contact-section`

- **hotfix/<issue>:** Ramas creadas desde `main` para corregir errores críticos detectados en la versión estable de la landing page.

El flujo de trabajo establece que cada rama `feature` debe integrarse a `develop` mediante **Pull Request (PR)** en GitHub, permitiendo revisión de código antes de aprobar la integración.

Cada commit debe seguir la convención de **Conventional Commits**, permitiendo una trazabilidad clara de los cambios realizados en el proyecto.

Ejemplos:

- `feat(home): implement hero section`
- `feat(contact): complete contact landing section`
- `fix(contact): polish mobile section layout`
- `refactor(landing): align Vue sections with mockups`
- `docs(readme): update GitFlow workflow`

### 5.1.3. Source Code Style Guide & Conventions.

En esta sección se establecen las convenciones de estilo y nomenclatura adoptadas para los lenguajes utilizados en el proyecto MarketGo: HTML, CSS, JavaScript, TypeScript (Vue.js), C# (.NET 10) y Gherkin. Se aplica nomenclatura en inglés para todos los elementos del código, siguiendo el Ubiquitous Language definido para el dominio de inventario y abastecimiento.

#### Referencias de Guías de Estilo Adoptadas

| Lenguaje/Tecnología | Guía de Estilo |
| :--- | :--- |
| HTML/CSS | [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html) (Google, s. f.-a) |
| JavaScript | [Google JavaScript Style Guide](https://google.github.io/styleguide/jsguide.html) (Google, s. f.-b) |
| TypeScript / Vue.js | [Vue.js Priority A Guide](https://vuejs.org/style-guide/rules-essential.html) (Vue.js, s. f.-b) |
| C# / .NET | [Microsoft C# Coding Conventions](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions) (Microsoft, s. f.) |
| Gherkin | [Gherkin Reference](https://cucumber.io/docs/gherkin/reference/) (Cucumber, s. f.) |

Se utiliza nomenclatura en inglés relacionada con las entidades del dominio de la landing page y la plataforma MarketGo, manteniendo nombres claros, consistentes y alineados al producto.
| Elemento                     | Convención             | Ejemplo                                             |
| :--------------------------- | :--------------------- | :-------------------------------------------------- |
| Componentes Vue              | PascalCase             | `HomeSection.vue`, `PricingSection.vue`             |
| Archivos de estilos CSS      | kebab-case             | `home-section.css`, `pricing-section.css`           |
| Variables / Métodos TS       | camelCase              | `activeSection`, `scrollToSection()`                |
| Constantes                   | SCREAMING_SNAKE_CASE   | `DEFAULT_LOCALE`, `CONTACT_EMAIL`                   |
| Rutas / IDs de secciones     | kebab-case             | `product-information`, `contact-section`            |
| Claves de i18n               | camelCase / dot.case   | `home.title`, `pricing.professionalPlan`            |
| Ramas Git feature            | kebab-case             | `feature/home-section`, `feature/contact-section`   |
| Commits                      | Conventional Commits   | `feat(home): implement hero section`                |

#### Sangría y Formato
* Se aplica una indentación de dos espacios para archivos web (HTML, CSS, TS) y de cuatro espacios para C# (estándar de Rider/Visual Studio).
* Las llaves de apertura en C# se colocan en una nueva línea (Estilo Allman), mientras que en TS/JS van en la misma línea (Estilo K&R).

---
### 5.1.4. Software Deployment Configuration.

Se especifica la configuración de despliegue para los entornos de MarketGo, garantizando alta disponibilidad para usuarios de la plataforma.

#### Landing Page - Azure
El despliegue de la landing page se documenta mediante la siguiente URL de Azure Static Web Apps (Microsoft, 2024).
* **URL:** https://agreeable-meadow-0a900b010.3.azurestaticapps.net/
## 5.2. Landing Page, Services & Applications Implementation.

### 5.2.1. Sprint 1.

#### 5.2.1.1. Sprint Planning 1.

| **Sprint Planning Sprint 1** |  |
|---|---|
| **Sprint Planning Background** |  |
| Date | 05/04/2026 |
| Time | 10:00 p.m. |
| Location | Discord / WhatsApp |
| Prepared By | Albino Florencio Cáceres Pizarro |
| Attendees | Albino Florencio Cáceres Pizarro<br>Matias Daniel Huaranga Romero<br>Winnie Lisbeth Merino Ordinola<br>Andre Sebastian Quispe Almonacid<br>Alexis Calin Torres Huaman |
| **Sprint Goal & User Stories** |  |
| **Sprint 1 Goal** | Our focus is on delivering the first marketing landing page of MarketGo, a product by MarketLab, that clearly communicates the value proposition regarding inventory management, batch tracking, product conservation alerts, and supplier-minimarket coordination.<br><br>We believe it delivers a clear, professional first impression for minimarket owners, administrators, and organic product providers, helping them understand how MarketGo centralizes daily inventory operations and improves operational traceability.<br><br>This will be confirmed when users can navigate through all core sections of the landing page, including Home, Product Description, Videos, Plans, and Contact, and can seamlessly request more information or contact the MarketLab team. |
| Sprint 1 Velocity | 14 Story Points |

<p>
  <strong>Repositorio:</strong>
  <a href="https://github.com/Market-Labs/landign-page">
    https://github.com/Market-Labs/landign-page
  </a>
</p>

#### 5.2.1.2. Aspect Leaders and Collaborators.

<p>
Esta matriz <strong>LACX</strong> identifica los aspectos principales del sprint y asigna responsabilidades de Líder (L) y Colaborador (C) para organizar al equipo de <strong>MarketLab</strong> durante el desarrollo de la landing page de <strong>MarketGo</strong>.
</p>

<table border="1" cellpadding="4" cellspacing="0" align="center">
  <thead>
    <tr>
      <th>Team Member</th>
      <th>Aspect: UI/UX & Visual Design</th>
      <th>Aspect: Vue Structure & Components</th>
      <th>Aspect: Content & i18n</th>
      <th>Aspect: GitFlow & Deployment</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Cáceres Pizarro, Albino Florencio</td>
      <td>L</td>
      <td>C</td>
      <td>C</td>
      <td>L</td>
    </tr>
    <tr>
      <td>Huaranga Romero, Matias Daniel</td>
      <td>C</td>
      <td>L</td>
      <td>C</td>
      <td>C</td>
    </tr>
    <tr>
      <td>Merino Ordinola, Winnie Lisbeth</td>
      <td>C</td>
      <td>C</td>
      <td>L</td>
      <td>C</td>
    </tr>
    <tr>
      <td>Quispe Almonacid, Andre Sebastian</td>
      <td>C</td>
      <td>C</td>
      <td>C</td>
      <td>C</td>
    </tr>
    <tr>
      <td>Torres Huaman, Alexis Calin</td>
      <td>C</td>
      <td>C</td>
      <td>C</td>
      <td>C</td>
    </tr>
  </tbody>
</table>

#### 5.2.1.3. Sprint Backlog 1.

El Sprint Backlog agrupa las tareas iniciales correspondientes al diseño, desarrollo y documentación de la landing page de **MarketGo**, producto de **MarketLab** orientado a la gestión de inventario, lotes, conservación y abastecimiento de productos orgánicos para minimarkets.

<div align="center">
  <img src="assets/chapter-05/sprintb1.png" alt="Sprint 1 Board Screenshot" width="100%">
  <p><em>Figura: Tablero del Sprint 1 en Jira Software (Proyecto MarketGo)</em></p>
</div>

| User Story Id | Title | Task Id | Title | Description | Estimation (Hours) | Assigned To | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **US00** | Landing Page Base | T001 | Implementación de Home Section | Desarrollo de la sección principal de la landing page en Vue, presentando la propuesta de valor de MarketGo para minimarkets. | 4h | Cáceres Pizarro, Albino Florencio | Done |
| **US00** | Product Information | T002 | Maquetación de descripción del producto | Implementación de la sección informativa sobre inventario, lotes, alertas de conservación, pedidos y accesos por rol. | 4h | Huaranga Romero, Matias Daniel | Done |
| **US00** | Videos Section | T003 | Implementación de sección de videos | Desarrollo del apartado visual para presentar al equipo y mostrar el funcionamiento general de MarketGo. | 3h | Merino Ordinola, Winnie Lisbeth | Done |
| **US00** | Pricing Section | T004 | Implementación de planes | Maquetación de los planes Básico, Profesional y Empresarial, incluyendo precios, beneficios y llamadas a la acción. | 3h | Quispe Almonacid, Andre Sebastian | Done |
| **US00** | Contact Section | T005 | Implementación del formulario de contacto | Desarrollo de la sección de contacto con datos del equipo, formulario para minimarkets y aceptación de política de privacidad. | 4h | Torres Huaman, Alexis Calin | Done |
| **US00** | Landing Page Architecture | T006 | Organización DDD y estructura Vue | Refactorización de carpetas siguiendo una arquitectura orientada por secciones, separando componentes, estilos, assets e internacionalización. | 5h | Cáceres Pizarro, Albino Florencio | Done |
| **US00** | GitFlow Setup | T007 | Configuración de ramas y commits | Organización de ramas feature, integración en develop y actualización de main aplicando Conventional Commits. | 3h | Cáceres Pizarro, Albino Florencio | Done |

#### 5.2.1.4. Development Evidence for Sprint Review.

<p>
  Resumen de los commits más relevantes en el repositorio de la Landing Page de <strong>MarketGo</strong>, producto desarrollado por <strong>MarketLab</strong>.
</p>

<table border="1" cellpadding="4" cellspacing="0">
  <thead>
    <tr>
      <th>Branch</th>
      <th>Commit Id</th>
      <th>Commit Message</th>
      <th>Committed on</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>feature/marketgo-landing-page</td>
      <td><code>d49b631</code></td>
      <td>refactor(landing): align Vue sections with mockups</td>
      <td>19-09-2026</td>
    </tr>
    <tr>
      <td>feature/contact-section</td>
      <td><code>a6446e1</code></td>
      <td>feat(contact): complete contact landing section</td>
      <td>19-09-2026</td>
    </tr>
    <tr>
      <td>feature/contact-section</td>
      <td><code>fbf450a</code></td>
      <td>fix(contact): render email outside i18n parser</td>
      <td>19-09-2026</td>
    </tr>
    <tr>
      <td>develop</td>
      <td><code>1f850de</code></td>
      <td>fix(contact): polish mobile section layout</td>
      <td>19-09-2026</td>
    </tr>
    <tr>
      <td>main</td>
      <td><code>1f850de</code></td>
      <td>fix(contact): polish mobile section layout</td>
      <td>19-09-2026</td>
    </tr>
  </tbody>
</table>

#### 5.2.1.5. Execution Evidence for Sprint Review.

Durante el Sprint 1, el equipo logró implementar con éxito el diseño, maquetación y despliegue de la Landing Page estática de **MarketGo**. A continuación, se presentan las evidencias visuales de la ejecución del producto de software, demostrando el cumplimiento de los Criterios de Aceptación de las Historias de Usuario planificadas:

**Evidencia 1: Home Section y Propuesta de Valor**

Se desarrolló la pantalla de inicio principal destacando la propuesta de valor de **MarketGo**: controlar el inventario antes de que sea tarde mediante alertas de vencimiento, condiciones de conservación y pedidos de abastecimiento para minimarkets orgánicos. La navegación superior permite acceder a las secciones principales de la landing page y el diseño respeta los lineamientos *responsive* para dispositivos móviles.

<div align="center">
  <img src="assets/chapter-05/execution-home.png" alt="Home Section Evidence" width="90%">
  <p><em>Figura: Vista principal de MarketGo desplegada en la Landing Page.</em></p>
</div>

**Evidencia 2: Sección de Descripción del Producto**

Se maquetó la sección informativa donde se presentan las principales capacidades de **MarketGo**, incluyendo inventario centralizado, control de lotes, alertas inteligentes, pedidos de abastecimiento y accesos por rol. Esta sección permite comunicar de forma clara cómo la plataforma ayuda a centralizar la operación diaria de un minimarket orgánico.

<div align="center">
  <img src="assets/chapter-05/execution-product-information.png" alt="Product Information Section Evidence" width="90%">
  <p><em>Figura: Sección de descripción del producto y funcionalidades principales.</em></p>
</div>

**Evidencia 3: Sección de Videos**

Se implementó una sección dedicada a presentar al equipo y mostrar el funcionamiento general de **MarketGo** mediante contenido audiovisual. Esta sección permite reforzar la confianza del usuario y explicar visualmente el propósito de la solución.

<div align="center">
  <img src="assets/chapter-05/execution-videos.png" alt="Videos Section Evidence" width="90%">
  <p><em>Figura: Sección de videos para presentación del equipo y demostración del producto.</em></p>
</div>

**Evidencia 4: Sección de Planes**

Se desarrolló la sección de planes comerciales, presentando las alternativas **Básico**, **Profesional** y **Empresarial**. Cada plan comunica de manera ordenada sus beneficios principales, permitiendo que los minimarkets identifiquen la opción más adecuada según su tamaño y necesidades operativas.

<div align="center">
  <img src="assets/chapter-05/execution-pricing.png" alt="Pricing Section Evidence" width="90%">
  <p><em>Figura: Sección de planes disponibles para los usuarios de MarketGo.</em></p>
</div>

**Evidencia 5: Sección de Contacto**

Se implementó la sección de contacto, incluyendo información de correo, WhatsApp, horario de atención y un formulario para que los minimarkets interesados puedan solicitar más información o agendar una demostración. Esta sección cumple el objetivo de facilitar la comunicación directa con el equipo de **MarketLab**.

<div align="center">
  <img src="assets/chapter-05/execution-contact.png" alt="Contact Section Evidence" width="90%">
  <p><em>Figura: Sección de contacto para solicitar información sobre MarketGo.</em></p>
</div>

#### 5.2.1.6. Services Documentation Evidence for Sprint Review.

<p>
  Dado que el Sprint 1 abarca únicamente contenido estático correspondiente a la Landing Page de marketing de <strong>MarketGo</strong>, la implementación y consumo de servicios backend para la gestión de inventario, lotes, conservación, pedidos y proveedores será abordada en sprints posteriores orientados al desarrollo de la plataforma web.
</p>

#### 5.2.1.7. Software Deployment Evidence for Sprint Review.

<p>
  <strong>URL de Producción:</strong>
  <a href="https://agreeable-meadow-0a900b010.3.azurestaticapps.net/">
    https://agreeable-meadow-0a900b010.3.azurestaticapps.net/
  </a>
</p>

#### 5.2.1.8. Team Collaboration Insights during Sprint.

<p>
  Durante este primer sprint, el esfuerzo principal del equipo de <strong>MarketLab</strong> se centró en la estructuración del proyecto, el diseño UX/UI, la implementación de la landing page, la organización de ramas mediante GitFlow y la documentación inicial del producto <strong>MarketGo</strong>. Por lo tanto, las evidencias de colaboración presentadas a continuación corresponden al trabajo realizado para construir la presencia digital inicial del producto.
</p>

<p>
  En primer lugar, el <strong>Historial de Commits</strong> del repositorio demuestra que el trabajo fue organizado mediante ramas feature y commits siguiendo la convención de <strong>Conventional Commits</strong>. Durante el sprint se realizaron cambios incrementales relacionados con la maquetación de secciones, la adaptación visual basada en los mockups, la internacionalización de contenido y la corrección de detalles responsive.
</p>

<div align="center">
  <img src="assets/chapter-05/commit-history-sprint1.png" alt="Commit History Evidence" width="90%">
  <p><em>Figura: Historial de commits demostrando el avance incremental de la landing page de MarketGo.</em></p>
</div>

<p>
  En segundo lugar, el gráfico de <strong>Visitors (Traffic)</strong> proporcionado por los Insights de GitHub permite evidenciar la actividad de consulta del repositorio. Las visitas y usuarios únicos reflejan que el equipo revisó recurrentemente el avance del proyecto, validando la estructura visual, el contenido de las secciones y la coherencia general de la landing page antes del despliegue.
</p>

<div align="center">
  <img src="assets/chapter-05/visitors-sprint1.png" alt="Traffic Visitors Graph" width="90%">
  <p><em>Figura: Gráfica de visitantes mostrando la revisión constante del repositorio por parte del equipo MarketLab.</em></p>
</div>

### 5.2.2. Sprint 2

#### 5.2.2.1. Sprint Planning 2.

La planificación del Sprint 2 se centró en definir el primer incremento del frontend web de MarketGo y el resultado que el equipo presentará en la revisión del sprint.

| **Sprint Planning Sprint 2** |  |
|---|---|
| **Sprint Planning Background** |  |
| Date | 2026-09-26 |
| Time | 10:00 p.m. |
| Location | Discord / WhatsApp |
| Prepared By | Albino Florencio Cáceres Pizarro |
| Attendees | Albino Florencio Cáceres Pizarro<br>Matias Daniel Huaranga Romero<br>Winnie Lisbeth Merino Ordinola<br>Andre Sebastian Quispe Almonacid<br>Alexis Calin Torres Huaman |
| Sprint 1 Review Summary | En el Sprint 1 se implementó y desplegó la primera versión de la landing page de MarketGo, con las secciones Home, información del producto, videos, planes y contacto. La entrega permitió presentar la propuesta de valor y comprobar la navegación inicial y la adaptación a distintos tamaños de pantalla. Este resultado sirve como punto de partida para construir el frontend de la aplicación web durante el Sprint 2. La evidencia disponible no registra comentarios específicos del Product Owner. |
| Sprint 1 Retrospective Summary | La documentación del Sprint 1 muestra trabajo incremental mediante ramas feature, commits convencionales y colaboración en diseño, contenido y despliegue. Para el Sprint 2 se propone reforzar la coordinación entre quienes implementan las pantallas, la navegación por roles y la integración visual, y revisar temprano la experiencia responsive antes de la Sprint Review. |
| **Sprint Goal & User Stories** |  |
| **Sprint 2 Goal** | Our focus is on developing and deploying the first navigable version of the MarketGo frontend web application for minimarket administrators and organic product suppliers. The sprint will translate the approved UX/UI designs into responsive screens, clear navigation for each role, and representative flows for the platform's core operations.<br><br>We believe this will give both user groups a concrete interface for exploring MarketGo's daily workflows and will let the team validate the usability and consistency of the frontend before expanding its integration with services.<br><br>This will be confirmed when the first frontend version is accessible in a deployed environment, its principal screens work on desktop and mobile, and the planned navigation and interaction flows can be demonstrated during the Sprint Review. |
| User Stories del tablero con puntos definidos | US-026 Registrar usuario (3 SP); US-027 Inicio de sesión (3 SP); US-028 Gestionar permisos por rol (5 SP); US-029 Controlar acceso según operación (5 SP); US-030 Dashboard general (5 SP). US-033 figura en Trello, pero no está estimada en el Product Backlog del capítulo 3. |
| Velocidad de referencia (Sprint 1) | 14 Story Points; se usa como antecedente, no como velocidad lograda en Sprint 2. |
| Sum of Story Points | 21 Story Points (3 + 3 + 5 + 5 + 5) para las cinco historias del tablero que tienen estimación en el capítulo 3. US-033 queda pendiente de incorporación y estimación en el Product Backlog. |

**Repositorio Landing Page:** https://github.com/Market-Labs/landign-page.git

**Repositorio Frontend:** https://github.com/Market-Labs/front-end.git

#### 5.2.2.2. Aspect Leaders and Collaborators.

Para el Sprint 2 se identificaron aspectos funcionales que corresponden a los bounded contexts implementados en el frontend, más un aspecto transversal de configuración del proyecto (Vue 3, Vite, Pinia e i18n). La siguiente matriz LACX recoge la asignación documentada para el Sprint 2. La captura general de Trello no permite verificar los responsables de todos los aspectos; los liderazgos deben contrastarse con las tarjetas asignadas y los commits de cada integrante.

| Team Member | IAM & Project Setup | Requisition & Procurement | Suppliers & Products | Inventory & Conservation | Dashboard & Profiles | Communication | Analytics |
|---|---|---|---|---|---|---|---|
| Cáceres Pizarro, Albino Florencio | L | C | C | C | L | C | C |
| Huaranga Romero, Matias Daniel | C | C | C | C | C | C | C |
| Merino Ordinola, Winnie Lisbeth | C | L | C | C | C | C | C |
| Quispe Almonacid, Andre Sebastian | C | L | C | L | C | C | C |
| Torres Huaman, Alexis Calin | C | C | C | C | L | L | C |

#### 5.2.2.3. Sprint Backlog 2.

El Sprint Backlog 2 agrupa los User Stories priorizados del Product Backlog que corresponden al primer release navegable del Frontend Web Application, organizados por bounded context. Se utilizó Trello Software como herramienta de control de estado.


<div align="center">
  <img src="assets/chapter-05/sprint-backlog-2.png" alt="Tablero Sprint Backlog 2 de MarketGo en Trello" width="100%">
  <p><strong>Figura: Tablero del Sprint 2 en Trello (Proyecto MarketGo)</strong><br><em>Nota. Elaboración propia.</em></p>
</div>

| User Story Id | Title | Task Id | Title | Description | Estimation (Hours) | Assigned To | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **US-026** | Registrar usuario | T008 | Implementar registro de usuarios | Implementación del formulario de registro de usuarios y validación de los datos ingresados para permitir el acceso controlado a MarketGo. | 4h | Cáceres Pizarro, Albino Florencio | To-Do |
| **US-027** | Inicio de sesión | T009 | Implementar inicio de sesión | Desarrollo de la interfaz de autenticación y validación de credenciales para permitir el acceso según el rol del usuario. | 4h | Cáceres Pizarro, Albino Florencio | To-Do |
| **US-026** | Registrar usuario | T010 | Crear perfil asociado al usuario | Implementación de la creación de un perfil vinculado a cada usuario registrado en MarketGo. | 3h | Cáceres Pizarro, Albino Florencio | To-Do |
| **US-028** | Gestionar permisos por rol | T011 | Configurar roles y permisos | Configuración de los roles del administrador de minimarket y proveedor, estableciendo los permisos correspondientes. | 4h | Cáceres Pizarro, Albino Florencio | To-Do |
| **US-029** | Controlar acceso según operación | T012 | Aplicar control de acceso por operación | Implementación de restricciones de acceso a las funcionalidades de pedidos, órdenes de envío e inventario según el rol del usuario. | 4h | Cáceres Pizarro, Albino Florencio | In-Progress |
| **US-030** | Dashboard general | T013 | Maquetar dashboard por rol | Diseño y desarrollo de la estructura visual del dashboard con información diferenciada para administradores y proveedores. | 4h | Torres Huaman, Alexis Calin | To-Do |
| **US-030** | Dashboard general | T014 | Definir indicadores iniciales del dashboard | Definición de indicadores operativos para visualizar información relevante sobre inventario, abastecimiento y operaciones según el rol. | 3h | Torres Huaman, Alexis Calin | In-Progress |
| **US-028** | Gestionar permisos por rol | T016 | Validar criterios de aceptación IAM | Verificación de los criterios de aceptación relacionados con registro, autenticación, roles y permisos de usuarios. | 3h | Cáceres Pizarro, Albino Florencio | To-Review |
| **US-030** | Dashboard general | T017 | Validar visualización de dashboard por rol | Validación de la información e indicadores mostrados en el dashboard según los permisos del administrador y proveedor. | 3h | Torres Huaman, Alexis Calin | To-Review |
| **US-033** | Solicitar información o demo | T018 | Documentar flujo de solicitud de demo | Documentación del proceso de solicitud de información o demostración mediante el formulario de contacto de la landing page. | 2h | Huaranga Romero, Matias Daniel | To-Fix |
| **US-026** | Registrar usuario | — | Definir historia de registro de usuario | Definición de la funcionalidad de registro de usuarios y sus criterios de aceptación para el Sprint 2. | 2h | Cáceres Pizarro, Albino Florencio | Stories |
| **US-027** | Inicio de sesión | — | Definir historia de inicio de sesión | Definición de los requisitos de autenticación y acceso a MarketGo según el rol del usuario. | 2h | Cáceres Pizarro, Albino Florencio | Stories |
| **US-028** | Gestionar permisos por rol | — | Definir historia de gestión de permisos | Definición de los permisos correspondientes a los diferentes roles del sistema. | 2h | Cáceres Pizarro, Albino Florencio | Stories |
| **US-029** | Controlar acceso según operación | — | Definir historia de control de acceso | Definición de restricciones de operaciones según los permisos asociados a cada rol. | 2h | Cáceres Pizarro, Albino Florencio | Stories |
| **US-030** | Dashboard general | — | Definir historia del dashboard general | Definición de la visualización de información y los indicadores correspondientes a cada rol. | 2h | Torres Huaman, Alexis Calin | Stories |
| **US-033** | Solicitar información o demo | — | Definir historia de solicitud de demo | Definición de los requisitos del formulario de contacto para solicitar información sobre MarketGo. | 2h | Huaranga Romero, Matias Daniel | Stories |
| **Tech** | Requisition Bounded Context | BC-001 | Definir Bounded Context de Requisition | Documentación y delimitación del contexto de pedidos de abastecimiento, sus responsabilidades y relaciones con los demás contextos del sistema. | 3h | Merino Ordinola, Winnie Lisbeth | Done |
| **Tech** | Procurements Bounded Context | BC-002 | Definir Bounded Context de Procurements | Documentación del contexto de gestión de abastecimiento y órdenes de envío, identificando sus responsabilidades y procesos. | 3h | Quispe Almonacid, Andre Sebastian | Done |
| **Tech** | Conservation Bounded Context | BC-003 | Definir Bounded Context de Conservation | Definición del contexto encargado del monitoreo de condiciones de almacenamiento, temperatura, humedad y alertas de conservación. | 3h | Quispe Almonacid, Andre Sebastian | Done |
| **Tech** | Sales Bounded Context | BC-004 | Definir Bounded Context de Sales | Documentación del contexto relacionado con las ofertas de productos y las operaciones comerciales de MarketGo. | 3h | Torres Huaman, Alexis Calin | Done |
| **Tech** | Dashboard Bounded Context | BC-005 | Definir Bounded Context de Dashboard | Identificación de las responsabilidades e indicadores del dashboard general para administradores y proveedores. | 3h | Torres Huaman, Alexis Calin | Done |
| **Tech** | Profiles Bounded Context | BC-006 | Definir Bounded Context de Profiles | Documentación del contexto de perfiles de usuario y su relación con IAM y los demás contextos de MarketGo. | 3h | Cáceres Pizarro, Albino Florencio | Done |
| **Tech** | Communication Bounded Context | BC-007 | Definir Bounded Context de Communication | Definición del contexto de comunicación, notificaciones y alertas relacionadas con las operaciones del sistema. | 3h | Torres Huaman, Alexis Calin | Done |

<p><em>Nota de trazabilidad.</em> El tablero de Trello incluye US-033, pero el Product Backlog documentado en el capítulo 3 termina en US-030. Las estimaciones en horas y los responsables de esta tabla requieren contrastarse con el detalle de cada tarjeta; la captura general solo muestra títulos y columnas.</p>


#### 5.2.2.4. Development Evidence for Sprint Review.

El siguiente cuadro reúne los 26 commits de <code>Market-Labs/front-end</code> presentes en <code>origin/main</code> desde la planificación del Sprint 2 (26-09-2026) hasta el 09-10-2026. Se usan la fecha y hora de <em>commit</em> registradas por Git, convertidas a la zona horaria de Lima (UTC-5). La columna <code>main</code> indica la rama en la que se verificaron; Git no conserva la rama original en el objeto commit.

| Repositorio | Rama verificada | Commit Id | Commit Message | Fecha y hora (Lima, UTC-5) |
|---|---|---|---|---|
| front-end | main | [f5e9d4c](https://github.com/Market-Labs/front-end/commit/f5e9d4cae6213bbae9164b6a0d0d289564ba3c6e) | Refactor alert center for i18n and styling updates | 09-10-2026 18:57 |
| front-end | main | [da1b357](https://github.com/Market-Labs/front-end/commit/da1b357e892ba7d713eff11644b51d127a11eaa1) | Refactor communication routes with Pinia store | 09-10-2026 18:54 |
| front-end | main | [fdc4c7a](https://github.com/Market-Labs/front-end/commit/fdc4c7aff65d2e8fca3b9a48354e43b835a019ed) | Refactor MessageAssembler to handle default values | 09-10-2026 18:53 |
| front-end | main | [b0f1dc4](https://github.com/Market-Labs/front-end/commit/b0f1dc4c60849f8f880342ade104e3c5a19e64ca) | Modify getNotifications to handle supplier alerts | 09-10-2026 18:52 |
| front-end | main | [6ff080f](https://github.com/Market-Labs/front-end/commit/6ff080f6c64d90d2c7b4d2d7cdda4aeefcdca56b) | Refactor communication store to handle Firebase mode | 09-10-2026 18:51 |
| front-end | main | [ac5d708](https://github.com/Market-Labs/front-end/commit/ac5d7086332a647849dd1813ce5ea44b04ab0ad3) | Add files via upload | 09-10-2026 18:43 |
| front-end | main | [2726351](https://github.com/Market-Labs/front-end/commit/27263515c7285c1f86d2ff02ec8f6734f9254034) | docs(iam): add jsdoc comments to access role model | 09-10-2026 18:33 |
| front-end | main | [095849b](https://github.com/Market-Labs/front-end/commit/095849b03e20098caca93f14ba05d1c243a2c7fe) | fix(procurements): open shipping order form from accepted request | 09-10-2026 08:08 |
| front-end | main | [cc66031](https://github.com/Market-Labs/front-end/commit/cc66031b67df19746a79b3726f2172f4a63ec7bd) | fix(requisition): create Firestore documents without denied reads | 09-10-2026 06:51 |
| front-end | main | [1d2cc47](https://github.com/Market-Labs/front-end/commit/1d2cc47dd47779ae993c72bb2a26f13e75312177) | fix(iam): wait for initial route before mounting app | 09-10-2026 05:24 |
| front-end | main | [04953dd](https://github.com/Market-Labs/front-end/commit/04953dd1450bb59a595f0cfaa6a66ebc9816a263) | fix(shared): use MarketGo logo as favicon | 09-10-2026 05:16 |
| front-end | main | [f5d8415](https://github.com/Market-Labs/front-end/commit/f5d841505bbbcd72f1a9560d5f70296f400b747b) | feat(inventory): track lot expiration and offers | 09-10-2026 01:39 |
| front-end | main | [51e6052](https://github.com/Market-Labs/front-end/commit/51e6052b856fba45e5b3d4347a170a15c9e9b84d) | fix(iam): count available organization roles | 09-10-2026 01:00 |
| front-end | main | [39ef675](https://github.com/Market-Labs/front-end/commit/39ef675dd1f5eb2190841aa01d7c23ae4803cd54) | feat(iam): add administrator and collaborator roles | 09-10-2026 00:57 |
| front-end | main | [5ae76e1](https://github.com/Market-Labs/front-end/commit/5ae76e12ffdc3c4e7001209c9ad303df51de5236) | fix(iam): validate signup email and explain failures | 08-10-2026 23:51 |
| front-end | main | [d8e8683](https://github.com/Market-Labs/front-end/commit/d8e868361c5d8e82e03aaefe326da7961e01abaf) | feat(iam): add tenant-scoped Firebase sign-up | 08-10-2026 23:37 |
| front-end | main | [c08ef33](https://github.com/Market-Labs/front-end/commit/c08ef3329db18501287da641569284718d1fd1df) | feat(suppliers): add sequential IDs and soft removal | 08-10-2026 23:03 |
| front-end | main | [56f891d](https://github.com/Market-Labs/front-end/commit/56f891dd4385497be6da3db01fcb2efbe33ec393) | feat(frontend): align inventory outputs and supply navigation | 08-10-2026 22:40 |
| front-end | main | [db37db8](https://github.com/Market-Labs/front-end/commit/db37db8174455672f3ad67d4f624ee7592ae59df) | Update README.md | 05-10-2026 13:27 |
| front-end | main | [df41d89](https://github.com/Market-Labs/front-end/commit/df41d8981060aeb8448d3702efeaf42f437d0336) | chore: edit frontend contract coverage | 05-10-2026 12:30 |
| front-end | main | [b91254a](https://github.com/Market-Labs/front-end/commit/b91254a50380098a97657d7aab1a0316f5300429) | chore : add news frontend contract Coverage | 05-10-2026 12:29 |
| front-end | main | [dff02e6](https://github.com/Market-Labs/front-end/commit/dff02e64ad4ca232f99a05b82538f7cd945dae43) | feat(firebase): persist MarketGo data and provision role-scoped users | 05-10-2026 11:53 |
| front-end | main | [890f87b](https://github.com/Market-Labs/front-end/commit/890f87bbce5c8810a18471b7781f7c5c9c7a0d19) | feat(shared): add read-only Azure demo mode | 03-10-2026 00:15 |
| front-end | main | [9705a3d](https://github.com/Market-Labs/front-end/commit/9705a3dc7f0635fb33da9c9c45553b0ba181ea9b) | chore(release): merge develop for Azure deployment | 02-10-2026 23:41 |
| front-end | main | [46e7f93](https://github.com/Market-Labs/front-end/commit/46e7f939815a71c47dc28dedf02d67fdc3fbd8d2) | docs(server): describe demo API and report endpoints | 02-10-2026 23:36 |
| front-end | main | [5f67499](https://github.com/Market-Labs/front-end/commit/5f6749987235358371810ed28b12e5b877ed788d) | feat(frontend): complete role-based workflows and reports | 02-10-2026 23:36 |

Las correcciones de la landing page fechadas el 19-09-2026 preceden a la planificación del Sprint 2; se documentan como antecedente y no como commits de este sprint.

#### 5.2.2.5. Execution Evidence for Sprint Review.

<p>
  Durante el Sprint 2, el equipo de MarketLab documentó los avances
  funcionales del Frontend Web Application de <strong>MarketGo</strong>,
  una plataforma orientada a la gestión de inventarios, productos,
  abastecimiento y conservación de productos orgánicos en minimarkets.
  La aplicación fue desarrollada con Vue 3, Vite y Pinia, y organizada
  mediante componentes, servicios y bounded contexts, con interfaces
  diferenciadas para los roles de Administrador de Minimarket y
  Proveedor. El repositorio organiza 12 módulos: 11 áreas
  funcionales y <strong>Shared</strong> como soporte transversal.
  El alcance documentado comprende:
</p>

<ul>
  <li>
    <strong>IAM (Identity and Access Management):</strong>
    Registro de usuarios, inicio de sesión, configuración de roles
    y permisos, y control de acceso a las operaciones del sistema
    según el tipo de usuario.
  </li>
  <li>
    <strong>Requisition:</strong>
    Gestión de pedidos de abastecimiento realizados por los
    administradores de minimarkets, permitiendo crear y consultar
    solicitudes de productos dirigidas a proveedores.
  </li>
  <li>
    <strong>Suppliers:</strong>
    Gestión y consulta del directorio de proveedores orgánicos,
    incluyendo información de contacto y productos disponibles
    para el abastecimiento de los minimarkets.
  </li>
  <li>
    <strong>Products:</strong>
    Catálogo de productos orgánicos con datos de nombre, precio,
    disponibilidad y características para las operaciones comerciales.
  </li>
  <li>
    <strong>Procurements:</strong>
    Gestión de pedidos y órdenes de envío, permitiendo que los
    proveedores acepten o rechacen solicitudes y que los
    administradores confirmen o rechacen la recepción de productos.
  </li>
  <li>
    <strong>Conservation:</strong>
    Consulta y monitoreo de las condiciones de conservación de
    productos mediante indicadores de temperatura y humedad,
    así como alertas relacionadas con condiciones de almacenamiento.
  </li>
  <li>
    <strong>Inventory:</strong>
    Visualización y administración del inventario de los
    minimarkets, incluyendo registro de productos, control
    de lotes, fechas de vencimiento y actualización de existencias.
  </li>
  <li>
    <strong>Dashboard:</strong>
    Panel general con indicadores operativos adaptados al rol
    del usuario, permitiendo visualizar información relevante
    sobre inventario, abastecimiento, productos y alertas.
  </li>
  <li>
    <strong>Analytics:</strong>
    Indicadores operativos y generación de reportes sobre inventario,
    abastecimiento, mermas, conservación y proveedores.
  </li>
  <li>
    <strong>Profiles:</strong>
    Gestión de perfiles de usuario asociados a las cuentas
    registradas, incluyendo información personal y datos
    correspondientes al administrador o proveedor.
  </li>
  <li>
    <strong>Communication:</strong>
    Visualización de mensajes, notificaciones y alertas
    relacionadas con las operaciones de abastecimiento,
    conservación e inventario.
  </li>
  <li>
    <strong>Shared:</strong>
    Infraestructura transversal para el layout, rutas, componentes
    reutilizables, internacionalización y adaptadores de datos.
  </li>
</ul>

<p>
  La aplicación contempla soporte de internacionalización
  <strong>i18n</strong> (español e inglés), una interfaz basada
  en Vue 3 y navegación mediante Vue Router. Asimismo,
  se trabajó en la validación de criterios de aceptación de IAM,
  la visualización del dashboard por rol y las mejoras de la
  Landing Page solicitadas por el docente, incluyendo la
  adaptación de las Historias de Usuario al rol
  <strong>Visitante (Visitor)</strong> y la incorporación de
  enlaces interactivos a LinkedIn, X y Facebook.
  A continuación, se incluyen las capturas representativas
  del Sprint Review.
</p>

<div align="center">
  <img src="assets/chapter-05/sprint2-signin.png" alt="Sign-In View" width="90%">
  <p><strong>Figura: Vista de inicio de sesión de MarketGo.</strong><br><em>Nota. Elaboración propia.</em></p>
</div>

<div align="center">
  <img src="assets/chapter-05/sprint2-requisitions.png" alt="Supply Requests View" width="90%">
  <p><strong>Figura: Solicitudes de abastecimiento de MarketGo.</strong><br><em>Nota. Elaboración propia.</em></p>
</div>

<div align="center">
  <img src="assets/chapter-05/sprint2-suppliers.png" alt="Supplier Directory" width="90%">
  <p><strong>Figura: Directorio de proveedores orgánicos de MarketGo.</strong><br><em>Nota. Elaboración propia.</em></p>
</div>

<p><em>La captura específica de órdenes de envío aún no se ha adjuntado a esta evidencia del Sprint 2.</em></p>

<div align="center">
  <img src="assets/chapter-05/sprint2-inventory.png" alt="Inventory Management" width="90%">
  <p><strong>Figura: Inventario de MarketGo con productos, lotes, existencias y vencimientos.</strong><br><em>Nota. Elaboración propia.</em></p>
</div>

<div align="center">
  <img src="assets/chapter-05/sprint2-dashboard.png" alt="MarketGo Dashboard" width="90%">
  <p><strong>Figura: Dashboard general de MarketGo con indicadores de inventario, abastecimiento y envíos.</strong><br><em>Nota. Elaboración propia.</em></p>
</div>

<h4>Product Navigation Video Evidence</h4>

<p>
  En esta sección se presenta el video demostrativo de navegación
  de la plataforma <strong>MarketGo</strong>, desarrollado por
  <strong>MarketLab</strong> como evidencia del Sprint 2.
  El propósito de este material audiovisual es mostrar los
  principales flujos del Frontend Web Application, incluyendo
  el registro e inicio de sesión, la gestión de perfiles,
  el acceso diferenciado según el rol, la administración
  del inventario, la consulta de proveedores, la gestión
  de pedidos de abastecimiento y órdenes de envío,
  así como la visualización de indicadores en el dashboard.
  Asimismo, se busca evidenciar la interacción entre los
  bounded contexts y la navegación general del sistema
  para los roles de Administrador de Minimarket y Proveedor.
  El material audiovisual puede alojarse en la plataforma
  institucional <strong>Microsoft Stream</strong>.
</p>

<strong>Nombre del archivo de video:</strong>
<code>marketgo-productnavigation-sprint-2.mp4</code>

<div align="center">
  <a href="https://upcedupe-my.sharepoint.com/:v:/g/personal/u201923820_upc_edu_pe/IQADWTad-EyvSqVDDT4XLbUfARe43Rpcn6uBFHpgZRcl68I?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=GlflNR" target="_blank">
    <img src="assets/chapter-05/tutorial-marketgo.png" alt="Video Demostrativo MarketGo en Microsoft Stream" width="90%" style="border: 1px solid #ccc; border-radius: 8px;">
  </a>
  <p><strong>Figura: Vista del video demostrativo de navegación de MarketGo.</strong><br><em>Nota. Elaboración propia.</em></p>
</div>

Enlace directo: https://upcedupe-my.sharepoint.com/:v:/g/personal/u201923820_upc_edu_pe/IQADWTad-EyvSqVDDT4XLbUfARe43Rpcn6uBFHpgZRcl68I?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJPbmVEcml2ZUZvckJ1c2luZXNzIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXciLCJyZWZlcnJhbFZpZXciOiJNeUZpbGVzTGlua0NvcHkifX0&e=GlflNR


#### 5.2.2.6. Services Documentation Evidence for Sprint Review.

El frontend de MarketGo está desarrollado con Vue 3, Vite y Pinia. El repositorio <code>Market-Labs/front-end</code> documenta dos fuentes de datos para validar los flujos de IAM, proveedores, inventario, abastecimiento, órdenes de envío y dashboard:

**Local (interfaz web):** http://localhost:5173/. Con <code>npm run dev:firebase</code> la interfaz utiliza Firebase; con <code>npm run dev:mock</code> utiliza la fake API de <code>json-server</code> en <code>http://localhost:3000</code>. Los dos puertos corresponden a procesos distintos.

| Entorno | Servicio de datos | Evidencia en el repositorio |
|---|---|---|
| Desarrollo local | <code>json-server</code> expone una fake API HTTP en <code>http://localhost:3000</code> al ejecutar <code>npm run dev:mock</code>. | <code>server/db.json</code>, <code>server/routes.json</code> y <code>server/README.md</code>. |
| Frontend publicado en Azure | Firebase Authentication gestiona el inicio de sesión y Cloud Firestore almacena los datos de demostración. La app se compila con <code>VITE_DATA_SOURCE=firebase</code> y usa el SDK de Firebase y un adaptador de Firestore. | <code>firebase.json</code>, <code>src/shared/infrastructure/firebase-client.js</code>, adaptadores de los bounded contexts y el workflow de Azure Static Web Apps. |

La siguiente tabla resume rutas comprobables de la fake API <strong>local</strong>. Son rutas del servidor de prueba; Firebase no publica estas rutas HTTP. Los contratos futuros de ASP.NET Core/C# descritos en el capítulo 3 no constituyen evidencia de un backend desplegado en este sprint.

| Funcionalidad | Ruta de la fake API local | Uso en MarketGo |
|---|---|---|
| Autenticación | <code>/api/v1/auth/*</code> | Simular las operaciones de acceso en desarrollo local. |
| Usuarios | <code>/api/v1/minimarkets/:minimarketId/users</code> | Consultar y administrar usuarios del minimarket. |
| Productos | <code>/api/v1/products</code> | Consultar y actualizar el catálogo. |
| Proveedores | <code>/api/v1/suppliers</code> | Consultar el directorio de proveedores. |
| Inventario | <code>/api/v1/minimarkets/:minimarketId/inventory</code> | Consultar y registrar existencias y lotes. |
| Solicitudes de abastecimiento | <code>/api/v1/minimarkets/:minimarketId/requisitions</code> | Crear y consultar solicitudes. |
| Órdenes de envío | <code>/api/v1/minimarkets/:minimarketId/purchase-orders</code> | Consultar y gestionar envíos. |
| Dashboard | <code>/api/v1/minimarkets/:minimarketId/dashboard</code> | Obtener indicadores para el administrador. |

En el entorno publicado, las operaciones equivalentes se realizan mediante Firebase Authentication y Firestore. El proyecto Firebase configurado en el cliente es <code>marketgo-d9c75</code>; no existe una URL pública de API REST de MarketGo que corresponda a la tabla local. La documentación de OpenAPI/Swagger pertenece al backend ASP.NET Core/C# planificado y no se presenta como servicio implementado en Sprint 2.

#### 5.2.2.7. Software Deployment Evidence for Sprint Review.

El Frontend Web Application de MarketGo se aloja en Azure Static Web Apps y utiliza Firebase Authentication y Cloud Firestore como servicios de datos de demostración. La aplicación es una SPA de Vue 3, Vite, Pinia y Vue Router. La fake API de <code>json-server</code> se ejecuta solo en desarrollo local; no es el servicio publicado en Azure ni un servidor alojado en Firebase.

| Componente | Configuración comprobada | Propósito |
|---|---|---|
| Frontend | El workflow <code>.github/workflows/azure-static-web-apps-ambitious-field-08f658810.yml</code> del repositorio <code>front-end</code> se ejecuta al hacer push a <code>main</code>, usa Azure Static Web Apps y publica la salida <code>dist</code>. | Alojar la interfaz web de MarketGo en Azure. |
| Datos de demostración | El workflow establece <code>VITE_DATA_SOURCE=firebase</code>; el cliente inicializa Firebase Authentication y Cloud Firestore para el proyecto <code>marketgo-d9c75</code>. | Autenticar usuarios y persistir los datos mostrados por el frontend desplegado. |
| Frontend local | <code>npm run dev</code> o <code>npm run dev:firebase</code> sirven la interfaz con Vite en <code>http://localhost:5173/</code>. | Revisar la aplicación desde el navegador durante el desarrollo. |
| Fake API local | <code>npm run dev:mock</code> inicia Vite en <code>http://localhost:5173/</code> y <code>json-server</code> en <code>http://localhost:3000</code>. | Probar la interfaz y los contratos HTTP sin el entorno publicado. |

El repositorio contiene además reglas de Firestore en <code>firestore.rules</code> y la configuración <code>firebase.json</code>. El workflow usa un secreto de GitHub para el token de Azure; su valor y el resultado de cada ejecución no pueden verificarse a partir de los archivos locales.

**URLs públicas del proyecto (comprobadas con respuesta HTTP 200 el 09-10-2026):**

- **Frontend Web Application:** https://ambitious-field-08f658810.2.azurestaticapps.net/
- **Landing page:** https://agreeable-meadow-0a900b010.3.azurestaticapps.net/

La landing page enlaza al inicio de sesión del frontend desde sus botones de acceso y demostración. El código de <code>HomeSection.vue</code> y <code>TheHeader.vue</code> usa la URL del frontend con la ruta <code>/login?redirect=/home</code>. Para completar la evidencia visual del despliegue queda por adjuntar una captura o enlace de la ejecución correcta del workflow de Azure y, si se requiere, una captura de la configuración de Firebase.

#### 5.2.2.8. Team Collaboration Insights during Sprint.

<p>
  Durante el Sprint 2, el equipo de <strong>MarketLab</strong>
  utilizó <strong>Trello</strong> para organizar y supervisar
  las actividades del desarrollo de MarketGo. El tablero permitió
  clasificar las tareas en columnas como <em>To-Do</em>,
  <em>In-Progress</em>, <em>To-Review</em>,
  <em>To-Fix</em> y <em>Done</em>,
  facilitando la identificación del estado de cada actividad,
  el seguimiento del avance y la coordinación entre los integrantes.
  Esta organización permitió mantener una visión general de
  las responsabilidades asociadas al Sprint Backlog.
</p>

<p>
  El trabajo se organizó por <em>bounded contexts</em>,
  distribuyendo las responsabilidades entre los cinco integrantes:
  <strong>Cáceres Pizarro, Albino Florencio</strong>,
  como líder general del equipo;
  <strong>Huaranga Romero, Matias Daniel</strong>;
  <strong>Merino Ordinola, Winnie Lisbeth</strong>;
  <strong>Quispe Almonacid, Andre Sebastian</strong>;
  y <strong>Torres Huaman, Alexis Calin</strong>.
  Esta distribución permitió trabajar en las funcionalidades
  y la documentación de IAM, Profiles, Requisition,
  Procurements, Suppliers, Products, Inventory,
  Conservation, Dashboard y Communication.
  La coordinación del equipo comprendió la asignación
  de tareas en Trello, el seguimiento de los avances,
  la integración de cambios en GitHub y la revisión
  de los entregables correspondientes al Sprint 2.
</p>

<p>Como evidencia de colaboración, la vista <em>Pulse</em> de GitHub Insights del repositorio <code>Market-Labs/front-end</code> muestra el periodo del 2 al 9 de octubre de 2026. En esa ventana, cuatro autores registraron 26 commits en <code>main</code> y 46 commits en todas las ramas, excluidos los merges. GitHub también registra 100 archivos modificados en <code>main</code>, con 8&nbsp;663 adiciones y 807 eliminaciones, además de una versión publicada. La captura indica cero pull requests fusionados o abiertos y cero issues nuevos o cerrados durante ese periodo. Los cuatro autores con commits no representan necesariamente a todos los cinco integrantes que participaron en el Sprint 2; la colaboración en tareas y documentación se registra por separado en Trello y en la matriz LACX.</p>

<div align="center">
  <img src="assets/chapter-05/sprint2-collaboration-insights.png" alt="GitHub Insights Pulse del repositorio front-end entre el 2 y el 9 de octubre de 2026" width="90%">
  <p><strong>Figura: Actividad de colaboración y commits del repositorio front-end durante el Sprint 2.</strong><br><em>Nota. Captura de GitHub Insights / Pulse del repositorio Market-Labs/front-end.</em></p>
</div>

<p>La vista <em>Traffic</em> del mismo repositorio muestra, para la ventana de 14 días indicada en la captura, 76 clonaciones realizadas por 40 clonadores únicos y 27 visualizaciones del repositorio por cuatro visitantes únicos. Estas métricas describen el acceso al repositorio de GitHub; no miden usuarios de MarketGo ni visitas a la aplicación o a la landing page. Tampoco permiten calcular Story Points completados.</p>

<div align="center">
  <img src="assets/chapter-05/sprint2-repository-traffic.png" alt="GitHub Insights Traffic con clonaciones y visitas del repositorio front-end" width="90%">
  <p><strong>Figura: Tráfico del repositorio front-end, con clonaciones y visualizaciones registradas por GitHub.</strong><br><em>Nota. Captura de GitHub Insights / Traffic del repositorio Market-Labs/front-end.</em></p>
</div>

<p><strong>Aciertos del Sprint:</strong></p>
<ul>
  <li>
    La organización del frontend por <em>bounded contexts</em>
    (<code>iam</code>, <code>profiles</code>,
    <code>products</code>, <code>suppliers</code>,
    <code>inventory</code>, <code>requisition</code>,
    <code>procurements</code>, <code>conservation</code>,
    <code>dashboard</code> y <code>communication</code>)
    permitió distribuir las responsabilidades entre
    los integrantes y mantener una separación clara
    de las funcionalidades del sistema.
  </li>
  <li>
    La organización de los adaptadores de datos facilitó el uso
    de Firebase Authentication y Firestore en el frontend publicado,
    junto con la fake API HTTP de desarrollo local,
    manteniendo la coherencia entre las operaciones
    de inventario, proveedores y abastecimiento.
  </li>
  <li>
    El uso de Vue 3, Vite y Pinia permitió establecer
    una arquitectura frontend basada en componentes
    reutilizables y gestión centralizada del estado.
    Asimismo, se consideró la internacionalización
    mediante <strong>i18n</strong> para ofrecer soporte
    en español e inglés.
  </li>
</ul>

<p><strong>Oportunidades de mejora identificadas:</strong></p>
<ul>
  <li>
    Reforzar la validación de formularios y los criterios
    de aceptación de IAM, especialmente en el registro
    de usuarios, inicio de sesión y asignación de permisos,
    para garantizar un comportamiento consistente
    según el rol.
  </li>
  <li>
    Mejorar la documentación de los componentes,
    stores de Pinia y adaptadores de Firebase y de la fake API local,
    estableciendo convenciones de nombres y
    responsabilidades claras entre los bounded contexts
    para facilitar el mantenimiento del código.
  </li>
  <li>
    Incrementar la cobertura de pruebas funcionales
    y de integración, principalmente en los flujos
    de pedidos de abastecimiento, órdenes de envío,
    actualización del inventario y visualización del
    dashboard según el rol del usuario.
  </li>
</ul>

### 5.2.3. Sprint 3

#### 5.2.3.1. Spring Planning 3.

La reunión de planificación del Sprint 3 se realizó el 7 de noviembre de 2026 a las 9:00 p. m. El equipo tomó como base la aplicación web presentada en el Sprint 2 y la estructura compartida del repositorio `Market-Labs/backend`. Se acordó trabajar los módulos de negocio mostrados en el tablero Sprint Backlog 3. La base existente aún requiere compilación y pruebas en un entorno con el SDK de .NET 10; los bounded contexts tienen sus carpetas preparadas, pero todavía no contienen lógica de negocio en la evidencia documentada.

| **Sprint Planning Sprint 3** |  |
|---|---|
| **Sprint Planning Background** |  |
| Date | 7 de noviembre de 2026 |
| Time | 9:00 p. m. (hora de Lima) |
| Location | Pendiente de registrar |
| Prepared By | Albino Florencio Cáceres Pizarro, team leader |
| Equipo considerado para la planificación | Albino Florencio Cáceres Pizarro<br>Matias Daniel Huaranga Romero<br>Winnie Lisbeth Merino Ordinola<br>Andre Sebastian Quispe Almonacid<br>Alexis Calin Torres Huaman |
| Sprint 2 Review Summary | El Sprint 2 dejó una aplicación frontend navegable para administradores de minimarkets y proveedores. El frontend se publicó en Azure Static Web Apps y utiliza Firebase Authentication y Firestore para el acceso y los datos de demostración. La fake API de `json-server` se utilizó en desarrollo local. El Sprint 2 no entregó Web Services propios de MarketGo. |
| Sprint 2 Retrospective Summary | Para integrar el frontend con servicios propios será necesario acordar contratos de datos, responsabilidades por bounded context y criterios de aceptación verificables antes de reemplazar los adaptadores de demostración. |
| **Sprint Goal & User Stories** |  |
| **Sprint 3 Goal** | Desarrollar los módulos de negocio de MarketGo sobre la base compartida del backend: inventario, productos de proveedores, pedidos de abastecimiento, órdenes de envío y recepción, conservación, alertas, ofertas y contacto comercial. El incremento se verificará mediante endpoints implementados, persistencia, pruebas y evidencia de integración con el frontend. |
| Historias y trabajos técnicos acordados | TECH 001 (base compartida; corresponde a IMP-BE-001 del capítulo III); US-001, US-002, US-010, US-011, US-012, US-014, US-015, US-016, US-018, US-019, US-021, US-023 y US-033. Se agrupan en las ocho tarjetas visibles del tablero Sprint Backlog 3. |
| Story Points comprometidos | **59 Story Points**, suma de las historias y del trabajo técnico seleccionados en el tablero Sprint Backlog 3 según las estimaciones del Product Backlog del capítulo III. Es una estimación planificada, no un total completado. |

La base compartida verificada contiene `Result`, contratos de repositorio y unidad de trabajo, `AppDbContext`, repositorios base, auditoría automática, convenciones de nombres, configuración CORS, OpenAPI/Scalar y `GET /api/v1/health`. En la consulta de ramas realizada para este apartado, el commit `8e71264` estaba en `develop` y en las ramas `feature/...` del backend; `origin/main` apuntaba a una versión anterior. No se presenta la base como compilada ni como un backend de negocio desplegado.

#### 5.2.3.2. Aspect Leaders and Collaborators.

Albino Florencio Cáceres Pizarro coordina el Sprint 3 como team leader y preparó la base compartida del backend. La siguiente matriz distribuye los bounded contexts para la planificación del trabajo pendiente. `L` identifica al líder planificado y `C` a un colaborador; fuera de la base compartida, estas asignaciones no constituyen evidencia de implementación completada.

| Team Member | Shared / API | Iam | Organizations | CatalogInventory | ConservationQuality | ProcurementOrders | AlertsNotifications | CommercialContact |
|---|---|---|---|---|---|---|---|---|
| Cáceres Pizarro, Albino Florencio | L | L | C | C | C | C | C | C |
| Huaranga Romero, Matias Daniel | C | C | L | C | C | C | C | L |
| Merino Ordinola, Winnie Lisbeth | C | C | C | C | C | L | C | C |
| Quispe Almonacid, Andre Sebastian | C | C | C | L | L | C | C | C |
| Torres Huaman, Alexis Calin | C | C | C | C | C | C | L | C |

#### 5.2.3.3. Sprint Backlog 3.

La reunión seleccionó ocho tarjetas para el Sprint Backlog 3. La captura del tablero identifica las historias; los Story Points se toman del Product Backlog del capítulo III. La suma expresa el trabajo planificado y no acredita su implementación. Las responsabilidades por bounded context se describen en 5.2.3.2 y se contrastarán con las asignaciones del tablero.

<div align="center">
  <img src="assets/chapter-05/sprint-backlog-3.png" alt="Tablero Trello Sprint Backlog 3 de MarketGo" width="75%">
  <p><strong>Figura: Tablero Sprint Backlog 3 con la meta y las ocho tarjetas seleccionadas.</strong><br><em>Nota. Captura del tablero Trello de MarketGo.</em></p>
</div>

| Tarjeta del tablero | Referencia en el capítulo III | Story Points | Alcance planificado |
|---|---|---:|---|
| TECH 001: Base compartida del backend | IMP-BE-001 | 3 | Preparar la estructura compartida y la configuración inicial de los Web Services. |
| US-001 y US-002: Registrar y visualizar inventario | US-001 (5) + US-002 (5) | 10 | Registrar productos en inventario y consultar sus existencias. |
| US-015 y US-016: Productos de proveedores | US-015 (5) + US-016 (5) | 10 | Consultar productos de proveedores y registrar los productos ofrecidos. |
| US-018 y US-019: Pedidos de abastecimiento | US-018 (5) + US-019 (3) | 8 | Crear y consultar pedidos de abastecimiento. |
| US-021 y US-023: Órdenes de envío y recepción | US-021 (5) + US-023 (5) | 10 | Crear órdenes de envío y aceptar su recepción para actualizar el inventario. |
| US-010 a US-012: Conservación y alertas | US-010 (3) + US-011 (5) + US-012 (5) | 13 | Consultar condiciones de conservación, monitorear temperatura y humedad y generar alertas de riesgo. |
| US-014: Registrar ofertas de productos | US-014 (3) | 3 | Registrar ofertas de productos disponibles. |
| US-033: Solicitar información o demo | US-033 (2) | 2 | Recibir solicitudes comerciales desde la landing page. |
| **Total planificado** | **Ocho tarjetas** | **59** | **Story Points del Product Backlog del capítulo III.** |

#### 5.2.3.4. Development Evidence for Sprint Review.

Esta tabla se completará con commits verificables de los repositorios backend y frontend. La rama indicada deberá corresponder a la referencia donde se compruebe cada commit; la fecha y el mensaje se transcribirán del historial Git. La base compartida se documentará separadamente de los Web Services de negocio cuando se seleccione la evidencia del sprint.

| Repositorio | Rama verificada | Commit Id | Commit Message | Fecha y hora | Funcionalidad evidenciada |
|---|---|---|---|---|---|
| Backend | Por registrar | Por registrar | Por registrar | Por registrar | Base compartida y compilación |
| Backend | Por registrar | Por registrar | Por registrar | Por registrar | Primeros servicios de negocio |
| Frontend | Por registrar | Por registrar | Por registrar | Por registrar | Integración con los servicios propios |

#### 5.2.3.5. Execution Evidence for Sprint Review.

Se registrarán capturas y resultados de ejecución únicamente después de probar el incremento. Cada evidencia deberá indicar el entorno, la acción realizada, el resultado observado y el enlace o archivo de respaldo.

| Escenario por verificar | Resultado esperado | Resultado observado | Evidencia |
|---|---|---|---|
| Inicio de la API y `GET /api/v1/health` | El servicio inicia y responde al control de salud. | Pendiente de ejecución | Pendiente de captura |
| Documentación OpenAPI/Scalar | El documento muestra solo los endpoints implementados y sus contratos reales. | Pendiente de ejecución | Pendiente de captura |
| Primer endpoint de negocio | La solicitud válida responde con datos persistidos y la inválida devuelve un error controlado. | Pendiente de implementación y ejecución | Pendiente de captura |
| Integración con el frontend | La aplicación consulta un servicio propio y muestra la respuesta correspondiente. | Pendiente de implementación y ejecución | Pendiente de captura |

#### 5.2.3.6. Services Documentation Evidence for Sprint Review.

El documento del capítulo III describe contratos **previstos**; este apartado registrará únicamente los Web Services que se implementen y se comprueben durante Sprint 3. La presencia de una ruta en el Product Backlog no constituye evidencia de que exista en el backend.

| Servicio implementado | Método y ruta comprobados | Autorización y datos | Respuesta y error verificados | Enlace o captura de documentación |
|---|---|---|---|---|
| Control de salud de la base API | `GET /api/v1/health` (definido en `Program.cs`; ejecución pendiente de verificar) | Público; no requiere datos de negocio | Pendiente de prueba | Pendiente |
| Primer servicio de negocio | Pendiente de implementación | Pendiente | Pendiente | Pendiente |
| Servicio de integración frontend | Pendiente de implementación | Pendiente | Pendiente | Pendiente |

#### 5.2.3.7. Software Deployment Evidence for Sprint Review.

El frontend y la landing page ya tienen despliegues documentados en Sprint 2. En este apartado se incorporará la evidencia de la nueva versión de ambos productos y del primer despliegue de Web Services cuando esté disponible. La configuración local de MySQL y el endpoint de salud no demuestran, por sí solos, un backend desplegado.

| Componente | Plataforma | URL / configuración de Sprint 3 | Evidencia de publicación | Estado verificado |
|---|---|---|---|---|
| Landing page | Azure Static Web Apps | Pendiente de revalidar URL y versión | Pendiente de captura o ejecución del workflow | Pendiente |
| Frontend Web Application | Azure Static Web Apps | Pendiente de revalidar URL y versión | Pendiente de captura o ejecución del workflow | Pendiente |
| Backend Web Services | Pendiente de definir | Pendiente | Pendiente | No se ha documentado despliegue |
| Base de datos de los Web Services | Pendiente de definir | Pendiente | Pendiente | No se ha documentado despliegue |

#### 5.2.3.8. Team Collaboration Insights during Sprint.

La matriz de líderes anterior expresa una distribución planificada. Los resultados de colaboración del Sprint 3 se completarán con evidencia del periodo correspondiente y se distinguirán de la actividad del Sprint 2.

| Evidencia | Periodo | Resultado verificable | Fuente o captura |
|---|---|---|---|
| Tarjetas asignadas y revisadas | Pendiente | Pendiente | Pendiente |
| Commits por integrante y rama | Pendiente | Pendiente | Pendiente |
| Pull requests y revisiones | Pendiente | Pendiente | Pendiente |
| Acuerdos, dificultades y mejoras de coordinación | Pendiente | Pendiente | Pendiente |

## 5.3. Validation Interviews.

Las entrevistas de validación permitieron recoger las opiniones de administradores de minimarkets y proveedores de productos orgánicos después de interactuar con la landing page y la aplicación web de MarketGo. Sus respuestas se resumen en 5.3.2. La evaluación heurística de la interfaz se documenta por separado en 5.3.3, con el formato indicado en el statement del proyecto.

### 5.3.1. Diseño de Entrevistas.

| Elemento | Diseño de la validación |
|---|---|
| Objetivo | Evaluar si la propuesta de valor de la landing page se entiende y si los flujos de la aplicación ofrecen información útil para inventario, abastecimiento y atención de pedidos. |
| Participantes | Tres administradores de minimarkets y tres proveedores de productos orgánicos entrevistados previamente durante el Needfinding. |
| Modalidad | Interacción con la landing page y la aplicación web, seguida de preguntas sobre claridad, utilidad y facilidad de uso. |
| Duración | La duración de cada entrevista aún está por registrar. |
| Instrumento | Guía de 12 preguntas por segmento, observación de acciones y dificultades, y registro de respuestas. |
| Evidencia | Respuestas transcritas y resumidas en 5.3.2; capturas, duración y enlaces de grabación en proceso de incorporación. |

**Recorrido para administradores:** explorar Inicio, información del producto, videos, planes y contacto de la landing; entrar en la aplicación con una cuenta de prueba de administrador; revisar dashboard, inventario, proveedores, solicitudes de abastecimiento y recepción.

**Preguntas para administradores de minimarkets**

1. Después de recorrer la landing page, ¿entendiste qué problema busca resolver MarketGo?
2. ¿La información del producto y los videos te ayudaron a comprender cómo podrías usarlo en tu minimarket?
3. Al revisar los planes, ¿te parece clara la información sobre sus costos y beneficios? ¿Qué explicarías mejor?
4. ¿Te resultó claro cómo pasar de la landing page al inicio de sesión de la aplicación?
5. Al entrar al dashboard, ¿entendiste qué representan los indicadores de inventario, solicitudes y envíos?
6. Al revisar el inventario, ¿pudiste identificar qué lotes tienen bajo stock o una fecha de vencimiento que requiere atención?
7. ¿La información de producto, lote, stock y vencimiento fue suficiente para decidir qué acción tomarías?
8. Al revisar la actividad reciente y las alertas, ¿pudiste reconocer qué situación atenderías primero?
9. ¿La información del directorio de proveedores te resultó útil para elegir a quién solicitar productos?
10. Después de crear una solicitud de abastecimiento, ¿quedó claro qué información se registró y cómo consultarías su estado?
11. Después de probar la aplicación, ¿qué tan fácil te resultó usarla para revisar inventario, proveedores y pedidos? ¿Qué partes fueron intuitivas y cuáles te generaron dudas?
12. Después de probar MarketGo, ¿la usarías para gestionar tu inventario y tus pedidos de abastecimiento? ¿Por qué?

**Recorrido para proveedores:** explorar la propuesta, videos, planes y contacto de la landing; entrar en la aplicación con una cuenta de prueba de proveedor; revisar dashboard, productos, inventario, solicitudes y órdenes de envío.

**Preguntas para proveedores de productos orgánicos**

1. Después de recorrer la landing page, ¿entendiste qué ofrece MarketGo a un proveedor?
2. ¿La información del producto y los videos explicaron con claridad cómo se relacionaría tu negocio con los minimarkets?
3. Al revisar los planes, ¿te parece clara la información sobre sus costos y beneficios? ¿Qué explicarías mejor?
4. ¿Te resultó claro cómo pasar de la landing page al registro o inicio de sesión de la aplicación?
5. Al entrar al dashboard, ¿entendiste qué información se muestra sobre solicitudes, órdenes y productos?
6. ¿La vista de productos te permitió comprender cómo consultar o mantener actualizado tu catálogo?
7. Al revisar el inventario, ¿la información de lotes y stock te ayudaría a confirmar la disponibilidad de un producto?
8. Al abrir una solicitud de abastecimiento, ¿contabas con la información necesaria para decidir si podías atenderla?
9. ¿Te resultaron claros los estados y las acciones para aceptar o rechazar una solicitud?
10. Al preparar una orden de envío, ¿la aplicación mostró los datos que necesitarías para coordinar el despacho?
11. Después de probar la aplicación, ¿qué tan fácil te resultó usarla? ¿Qué partes te parecieron intuitivas y cuáles te generaron dudas?
12. Después de probar MarketGo, ¿la usarías para gestionar las solicitudes y pedidos de tus clientes? ¿Por qué?

### 5.3.2. Registro de Entrevistas.

Las seis entrevistas de validación se realizaron con los participantes del Needfinding (apartado 2.2.2) el 9 de noviembre de 2026. Los resúmenes siguientes sintetizan las respuestas de las transcripciones proporcionadas para cada participante. Las capturas, duraciones y URL de grabación están en proceso de incorporación.

<table style="width:100%; border-collapse:collapse;" border="1">
  <tbody>
    <tr><td colspan="4" align="center"><strong>Entrevista N.° 1</strong></td></tr>
    <tr><td colspan="4" align="center">Captura de la entrevista pendiente de incorporar.</td></tr>
    <tr><td colspan="2" align="center"><strong>Información del entrevistado</strong></td><td colspan="2" align="center"><strong>Contexto de validación</strong></td></tr>
    <tr><td><strong>Nombre completo</strong></td><td>Rodrigo Guevara</td><td><strong>Segmento objetivo</strong></td><td>Administrador de minimarket</td></tr>
    <tr><td><strong>Edad</strong></td><td>26 años</td><td><strong>Producto validado</strong></td><td>Landing page y Frontend Web Application de MarketGo</td></tr>
    <tr><td><strong>Ubicación</strong></td><td>José Leonardo Ortiz, Chiclayo, Lambayeque</td><td><strong>Duración</strong></td><td>Pendiente de registrar</td></tr>
    <tr><td><strong>Cargo</strong></td><td>Administrador general</td><td><strong>Fecha</strong></td><td>9 de noviembre de 2026</td></tr>
    <tr><td colspan="4"><strong>URL de grabación:</strong> Pendiente de incorporar.</td></tr>
    <tr><td colspan="4"><strong>Resumen de la entrevista</strong><br><br>Rodrigo comprendió la propuesta de centralizar inventario y pedidos y encontró claro el acceso desde la landing page. Los videos, el dashboard, la información de lotes y vencimientos, el directorio de proveedores y el seguimiento de solicitudes le resultaron útiles para reducir las revisiones manuales y la dispersión entre Excel, POS, libreta y WhatsApp. Señaló que convendría explicar mejor qué funciones incluye cada plan, mostrar cómo registrar un producto, añadir la fecha de ingreso de cada lote y ordenar las alertas por prioridad. También pidió acceso directo desde los indicadores, tiempos de entrega de proveedores y avisos cuando cambie el estado de una solicitud. Le tomó tiempo distinguir entre solicitudes y envíos; indicó que usaría la plataforma para gestionar inventario y abastecimiento.</td></tr>
  </tbody>
</table>

<table style="width:100%; border-collapse:collapse;" border="1">
  <tbody>
    <tr><td colspan="4" align="center"><strong>Entrevista N.° 2</strong></td></tr>
    <tr><td colspan="4" align="center">Captura de la entrevista pendiente de incorporar.</td></tr>
    <tr><td colspan="2" align="center"><strong>Información del entrevistado</strong></td><td colspan="2" align="center"><strong>Contexto de validación</strong></td></tr>
    <tr><td><strong>Nombre completo</strong></td><td>Roly Hans Luna</td><td><strong>Segmento objetivo</strong></td><td>Administrador de minimarket orgánico</td></tr>
    <tr><td><strong>Edad</strong></td><td>28 años</td><td><strong>Producto validado</strong></td><td>Landing page y Frontend Web Application de MarketGo</td></tr>
    <tr><td><strong>Ubicación</strong></td><td>San Isidro, Lima</td><td><strong>Duración</strong></td><td>Pendiente de registrar</td></tr>
    <tr><td><strong>Cargo</strong></td><td>Administrador de minimarket orgánico</td><td><strong>Fecha</strong></td><td>9 de noviembre de 2026</td></tr>
    <tr><td colspan="4"><strong>URL de grabación:</strong> Pendiente de incorporar.</td></tr>
    <tr><td colspan="4"><strong>Resumen de la entrevista</strong><br><br>Roly identificó la utilidad de MarketGo para controlar productos perecibles, existencias y pedidos. Valoró la lectura rápida del dashboard, los lotes y vencimientos, las alertas y el estado de las solicitudes; consideró especialmente importante recibir avisos de conservación y vencimiento en el celular. Solicitó mayor claridad sobre los límites de cada plan y demostraciones de uso móvil. Propuso mostrar condiciones de conservación junto al lote, destacar productos próximos a vencer, informar precios, disponibilidad y tiempos de entrega de proveedores, y contemplar recepciones parciales y correcciones de cantidades. Consideraría usar la aplicación si mantiene una experiencia cómoda desde el teléfono y reduce el trabajo manual con Excel y WhatsApp.</td></tr>
  </tbody>
</table>

<table style="width:100%; border-collapse:collapse;" border="1">
  <tbody>
    <tr><td colspan="4" align="center"><strong>Entrevista N.° 3</strong></td></tr>
    <tr><td colspan="4" align="center">Captura de la entrevista pendiente de incorporar.</td></tr>
    <tr><td colspan="2" align="center"><strong>Información del entrevistado</strong></td><td colspan="2" align="center"><strong>Contexto de validación</strong></td></tr>
    <tr><td><strong>Nombre completo</strong></td><td>María Fernanda Rojas Castillo</td><td><strong>Segmento objetivo</strong></td><td>Administradora de minimarket</td></tr>
    <tr><td><strong>Edad</strong></td><td>38 años</td><td><strong>Producto validado</strong></td><td>Landing page y Frontend Web Application de MarketGo</td></tr>
    <tr><td><strong>Ubicación</strong></td><td>Santiago de Surco, Lima</td><td><strong>Duración</strong></td><td>Pendiente de registrar</td></tr>
    <tr><td><strong>Cargo</strong></td><td>Administradora de minimarket</td><td><strong>Fecha</strong></td><td>9 de noviembre de 2026</td></tr>
    <tr><td colspan="4"><strong>URL de grabación:</strong> Pendiente de incorporar.</td></tr>
    <tr><td colspan="4"><strong>Resumen de la entrevista</strong><br><br>María Fernanda entendió la propuesta de organizar inventario y abastecimiento en una sola plataforma y encontró claro el paso de la landing page al inicio de sesión. Valoró el dashboard, la consulta de lotes, el directorio de proveedores y los estados de las solicitudes para dar seguimiento a varios pedidos. Solicitó precisar las funciones y posibles costos adicionales de los planes, añadir un ejemplo completo de recepción y explicar brevemente los indicadores. También sugirió mostrar el historial de movimientos de cada lote y de pedidos por proveedor, diferenciar alertas urgentes y aclarar cómo corregir una solicitud ya enviada. Indicó que evaluaría adoptar MarketGo si la gestión resulta sencilla y confiable.</td></tr>
  </tbody>
</table>

<table style="width:100%; border-collapse:collapse;" border="1">
  <tbody>
    <tr><td colspan="4" align="center"><strong>Entrevista N.° 4</strong></td></tr>
    <tr><td colspan="4" align="center">Captura de la entrevista pendiente de incorporar.</td></tr>
    <tr><td colspan="2" align="center"><strong>Información del entrevistado</strong></td><td colspan="2" align="center"><strong>Contexto de validación</strong></td></tr>
    <tr><td><strong>Nombre completo</strong></td><td>Álvaro Chojaga</td><td><strong>Segmento objetivo</strong></td><td>Proveedor de productos orgánicos</td></tr>
    <tr><td><strong>Edad</strong></td><td>54 años</td><td><strong>Producto validado</strong></td><td>Landing page y Frontend Web Application de MarketGo</td></tr>
    <tr><td><strong>Ubicación</strong></td><td>Miraflores, Lima</td><td><strong>Duración</strong></td><td>Pendiente de registrar</td></tr>
    <tr><td><strong>Cargo</strong></td><td>Administrador / jefe de operaciones y ventas</td><td><strong>Fecha</strong></td><td>9 de noviembre de 2026</td></tr>
    <tr><td colspan="4"><strong>URL de grabación:</strong> Pendiente de incorporar.</td></tr>
    <tr><td colspan="4"><strong>Resumen de la entrevista</strong><br><br>Álvaro comprendió que MarketGo permite organizar el catálogo y coordinar solicitudes de minimarkets, funciones que hoy gestiona con Excel y WhatsApp. Le resultaron claros el acceso, el dashboard, el catálogo, la consulta de stock y las acciones principales de las solicitudes. Pidió un video del flujo completo, límites de productos y clientes por plan, actualización sencilla de precios y cantidades, y avisos cuando el stock no alcance. Para coordinar entregas sugirió registrar la fecha solicitada, el destino y observaciones de transporte. También pidió confirmar antes de rechazar, registrar el motivo del rechazo y explicar mejor la diferencia entre solicitud aceptada y orden de envío. Consideraría utilizar la plataforma para ordenar sus operaciones.</td></tr>
  </tbody>
</table>

<table style="width:100%; border-collapse:collapse;" border="1">
  <tbody>
    <tr><td colspan="4" align="center"><strong>Entrevista N.° 5</strong></td></tr>
    <tr><td colspan="4" align="center">Captura de la entrevista pendiente de incorporar.</td></tr>
    <tr><td colspan="2" align="center"><strong>Información del entrevistado</strong></td><td colspan="2" align="center"><strong>Contexto de validación</strong></td></tr>
    <tr><td><strong>Nombre completo</strong></td><td>Luz Rojas</td><td><strong>Segmento objetivo</strong></td><td>Proveedora de productos orgánicos</td></tr>
    <tr><td><strong>Edad</strong></td><td>47 años</td><td><strong>Producto validado</strong></td><td>Landing page y Frontend Web Application de MarketGo</td></tr>
    <tr><td><strong>Ubicación</strong></td><td>Miraflores, Lima</td><td><strong>Duración</strong></td><td>Pendiente de registrar</td></tr>
    <tr><td><strong>Cargo</strong></td><td>Comerciante / mayorista de productos orgánicos</td><td><strong>Fecha</strong></td><td>9 de noviembre de 2026</td></tr>
    <tr><td colspan="4"><strong>URL de grabación:</strong> Pendiente de incorporar.</td></tr>
    <tr><td colspan="4"><strong>Resumen de la entrevista</strong><br><br>Luz entendió la utilidad de organizar productos y pedidos en MarketGo y valoró poder consultar solicitudes sin depender de conversaciones de WhatsApp. Consideró claros el acceso, el dashboard, el catálogo, el inventario y las acciones de aceptar o rechazar, especialmente para trabajar desde el teléfono. Solicitó ejemplos breves para explicar los planes, acceso móvil visible, identificación de pedidos recientes y edición rápida de precios. Propuso resumir cantidades antes de confirmar solicitudes, explicar el motivo de un rechazo y mostrar dirección y teléfono de contacto para el despacho. Tuvo dudas sobre cómo modificar una orden cuando cambia la cantidad pedida; indicó que usaría la aplicación si puede gestionar esas operaciones fácilmente desde el celular.</td></tr>
  </tbody>
</table>

<table style="width:100%; border-collapse:collapse;" border="1">
  <tbody>
    <tr><td colspan="4" align="center"><strong>Entrevista N.° 6</strong></td></tr>
    <tr><td colspan="4" align="center">Captura de la entrevista pendiente de incorporar.</td></tr>
    <tr><td colspan="2" align="center"><strong>Información del entrevistado</strong></td><td colspan="2" align="center"><strong>Contexto de validación</strong></td></tr>
    <tr><td><strong>Nombre completo</strong></td><td>Anita Gamboa</td><td><strong>Segmento objetivo</strong></td><td>Proveedora de productos orgánicos</td></tr>
    <tr><td><strong>Edad</strong></td><td>32 años</td><td><strong>Producto validado</strong></td><td>Landing page y Frontend Web Application de MarketGo</td></tr>
    <tr><td><strong>Ubicación</strong></td><td>Cerro Colorado, Arequipa</td><td><strong>Duración</strong></td><td>Pendiente de registrar</td></tr>
    <tr><td><strong>Cargo</strong></td><td>Proveedora de productos orgánicos</td><td><strong>Fecha</strong></td><td>9 de noviembre de 2026</td></tr>
    <tr><td colspan="4"><strong>URL de grabación:</strong> Pendiente de incorporar.</td></tr>
    <tr><td colspan="4"><strong>Resumen de la entrevista</strong><br><br>Anita comprendió la propuesta de centralizar catálogo, disponibilidad y seguimiento de pedidos. Valoró los videos, el dashboard, el inventario y la vista de solicitudes para reducir verificaciones repetidas entre Excel y WhatsApp. Pidió aclarar las diferencias entre planes y los roles de registro, filtrar productos por disponibilidad y señalar cuando una solicitud supere el stock. También sugirió conservar el historial de cambios, mostrar pedidos pendientes de despacho y registrar destino y fecha de entrega en las órdenes. La sección de solicitudes le resultó intuitiva, aunque tuvo dudas sobre cambios posteriores a la aceptación. Consideró útil MarketGo para coordinar mejor los pedidos si mantiene actualizados sus datos.</td></tr>
  </tbody>
</table>

### 5.3.3. Evaluaciones según heurísticas.

**Evaluación de User Experience según heurísticas — MarketGo**

**UX Heuristics & Principles Evaluation**
**Usabilidad · Diseño inclusivo · Arquitectura de información**

| Dato | Valor |
|---|---|
| Carrera | Ingeniería de Software |
| Curso | Aplicaciones Web |
| Sección | 8130 |
| Profesores | Oscar Ivan Villafuerte Bazan |
| Auditor | Grupo 3 (MarketLabs) |
| Cliente(s) | Rodrigo Guevara, Roly Hans Luna y María Fernanda Rojas Castillo |
| Fecha de evaluación | 9 de noviembre de 2026 |

#### Sitio o aplicación a evaluar

**MarketGo**, sistema web para la gestión de productos orgánicos: [ambitious-field-08f658810.2.azurestaticapps.net](https://ambitious-field-08f658810.2.azurestaticapps.net/home). La revisión se realizó con una cuenta de administrador proporcionada para esta evaluación. No se incluyen credenciales en este informe.

#### Tareas a evaluar

El alcance de esta evaluación incluye la revisión exploratoria de las siguientes tareas:

1. Iniciar sesión y consultar el estado general del negocio en el panel principal.
2. Consultar existencias, lotes, fechas de vencimiento y estados del inventario.
3. Localizar productos y reconocer su categoría, precio y disponibilidad.
4. Consultar solicitudes de abastecimiento y abrir el formulario de nueva solicitud, sin enviarlo.
5. Consultar el listado y estado de las entregas.
6. Revisar registros de temperatura y humedad en Conservación.
7. Revisar las alertas y cambiar la interfaz al español.

No se incluyen en esta versión las siguientes tareas:

1. Crear, editar o eliminar productos, stock, proveedores, usuarios o roles.
2. Enviar solicitudes, aceptar o rechazar entregas, o marcar alertas como leídas.
3. Evaluar procesos con otros perfiles de usuario o validar la interfaz mediante sesiones observadas con participantes.

**Método y alcance.** Auditoría heurística exploratoria de la interfaz visible en escritorio, con navegación de lectura y capturas de pantalla. Los hallazgos describen lo observado el 9 de noviembre de 2026; no son resultados de pruebas con usuarios ni de una auditoría técnica completa de accesibilidad. Esta versión del informe presenta únicamente problemas de severidad 2, conforme al alcance solicitado.

#### Escala de severidad

| Nivel | Descripción |
|---|---|
| 1 | **Problema superficial.** Se supera con facilidad o aparece muy rara vez; puede corregirse cuando haya tiempo disponible. |
| 2 | **Problema menor.** Aparece con cierta frecuencia o requiere esfuerzo adicional; prioridad baja para la siguiente versión. |
| 3 | **Problema mayor.** Aparece con frecuencia o dificulta seriamente la tarea; prioridad alta de corrección. |
| 4 | **Problema muy grave.** Impide continuar utilizando la herramienta; debe corregirse antes del lanzamiento. |

#### Tabla resumen

| # | Problema | Escala de severidad | Heurística o principio vulnerado |
|---|---|---:|---|
| 1 | El brócoli aparece clasificado como fruta en el catálogo. | 2 | Arquitectura de información: ¿es encontrable? y ¿es comprensible? |
| 2 | El listado de abastecimiento utiliza identificadores largos y formatos distintos para la misma clase de solicitud. | 2 | Arquitectura de información: ¿es usable?; usabilidad: reconocimiento antes que recuerdo. |
| 3 | El indicador “87 % estado general” no explica qué mide ni cómo se calcula. | 2 | Usabilidad: visibilidad del estado del sistema; ayuda y documentación. |
| 4 | Los botones de estrella de Alertas no comunican su función mediante un nombre accesible. | 2 | Diseño inclusivo: proporcionar experiencias comparables. |
| 5 | Alertas combina formatos de fecha distintos para registros del mismo listado. | 2 | Usabilidad: consistencia y estándares. |

#### Descripción de problemas

**Problema #1: categoría incorrecta para el brócoli**

**Severidad:** 2
**Principio vulnerado:** Arquitectura de información — ¿es encontrable? y ¿es comprensible?

**Problema.** En [Productos](https://ambitious-field-08f658810.2.azurestaticapps.net/products), el producto **“Brocoli”** con código **FRT-00003** aparece bajo la categoría **FRUTAS**, mientras **“Brocoli orgánico”** aparece en **VEGETALES**. Esta clasificación contradictoria dificulta localizar y comparar productos de la misma familia y puede inducir errores al organizar el catálogo.

**Captura:** catálogo de Productos.

<div align="center">
  <img src="assets/chapter-05/evidencias-heuristicas/03-productos.png" alt="Catálogo de productos orgánicos y clasificación del brócoli" width="55%">
  <p><strong>Figura: Catálogo de productos orgánicos y clasificación del brócoli.</strong><br><em>Nota. Captura de MarketGo; elaboración propia.</em></p>
</div>

**Recomendación.** Corregir la categoría del registro y validar la taxonomía al crear o editar productos. Revisar posibles duplicados semánticos antes de ofrecerlos en búsquedas o filtros.

**Problema #2: identificadores de solicitudes poco legibles e inconsistentes**

**Severidad:** 2
**Principio vulnerado:** Arquitectura de información — ¿es usable?; usabilidad — reconocimiento antes que recuerdo.

**Problema.** En [Abastecimiento](https://ambitious-field-08f658810.2.azurestaticapps.net/requisition), la columna “Solicitud” mezcla identificadores breves como **req-1** con otros de longitud UUID, como **req-0ac09682-9dbd-4b9d-b0a0-52818478338e**. Los identificadores largos ocupan gran parte de la fila y son difíciles de recordar, comparar o comunicar verbalmente. La tabla no muestra una referencia corta equivalente para esas solicitudes.

**Captura:** tabla de Abastecimiento.

<div align="center">
  <img src="assets/chapter-05/evidencias-heuristicas/04-abastecimiento.png" alt="Listado de solicitudes de abastecimiento con identificadores de distintos formatos" width="80%">
  <p><strong>Figura: Listado de solicitudes de abastecimiento con identificadores de distintos formatos.</strong><br><em>Nota. Captura de MarketGo; elaboración propia.</em></p>
</div>

**Recomendación.** Mostrar un número de solicitud uniforme, corto y único como referencia principal. Conservar el identificador técnico en el detalle o como dato copiable, junto con fecha de creación y proveedor para facilitar la distinción entre solicitudes.

**Problema #3: porcentaje de estado general sin significado explícito**

**Severidad:** 2
**Heurística vulnerada:** Usabilidad — visibilidad del estado del sistema; ayuda y documentación.

**Problema.** El [Dashboard](https://ambitious-field-08f658810.2.azurestaticapps.net/home) destaca **“87 % estado general”**, pero no indica qué dimensiones, período ni fórmula componen ese porcentaje. Un administrador no puede interpretar si representa inventario, abastecimiento, conservación o una combinación de ellos, ni entender qué acción lo mejoraría.

**Captura:** indicador de estado general.

<div align="center">
  <img src="assets/chapter-05/evidencias-heuristicas/01-dashboard.png" alt="Dashboard de MarketGo con indicador de estado general" width="80%">
  <p><strong>Figura: Dashboard de MarketGo con indicador de estado general.</strong><br><em>Nota. Captura de MarketGo; elaboración propia.</em></p>
</div>

**Recomendación.** Definir el indicador junto al valor, con un desglose de componentes y fecha de cálculo. Si no existe una métrica validada, evitar presentar un porcentaje que sugiera precisión sin contexto.

**Problema #4: botones de estrella sin nombre accesible**

**Severidad:** 2
**Principio vulnerado:** Diseño inclusivo — proporcionar experiencias comparables.

**Problema.** En el [Centro de alertas](https://ambitious-field-08f658810.2.azurestaticapps.net/communication), cada tarjeta contiene un botón representado visualmente por una estrella. En el árbol de accesibilidad, estos botones se exponen solo con el glifo del icono, sin un nombre que indique la acción. Esto obliga a quien utiliza un lector de pantalla a adivinar la función de un control secundario. La captura ilustra la ubicación de los botones; la falta de nombre se verificó en la representación de accesibilidad del navegador.

**Captura:** botones de estrella de Alertas.

<div align="center">
  <img src="assets/chapter-05/evidencias-heuristicas/06-alertas.png" alt="Centro de alertas de MarketGo con botones de estrella y formatos de fecha" width="55%">
  <p><strong>Figura: Centro de alertas de MarketGo con botones de estrella y formatos de fecha.</strong><br><em>Nota. Captura de MarketGo; elaboración propia.</em></p>
</div>

**Recomendación.** Asignar a cada botón un nombre accesible que describa su función real y actualizarlo cuando cambie su estado. Comprobarlo con navegación por teclado y lector de pantalla.

**Problema #5: formatos de fecha mezclados en Alertas**

**Severidad:** 2
**Heurística vulnerada:** Usabilidad — consistencia y estándares.

**Problema.** En el mismo [Centro de alertas](https://ambitious-field-08f658810.2.azurestaticapps.net/communication), las alertas antiguas muestran fechas como **2026-09-18 09:35**, mientras las de vencimiento muestran **9/11/2026, 12:46:40 p. m.**. La mezcla de formato ISO y fecha numérica local dificulta comparar la cronología y puede volver ambiguo el orden día/mes para lectores de distintas regiones.

**Captura:** fechas del Centro de alertas.

La figura del Centro de alertas incluida en el problema #4 también muestra los formatos de fecha descritos aquí.

**Recomendación.** Usar un formato único y localizado en todo el listado, por ejemplo “9 nov 2026, 12:46”, e incluir la zona horaria si las alertas pueden proceder de ubicaciones distintas.

#### Prioridad de corrección

1. Corregir la categoría del brócoli y normalizar las referencias de solicitudes.
2. Explicar el indicador de estado general, dar nombre accesible a los botones de estrella y unificar los formatos de fecha en Alertas.

## 5.4. Video About-the-Product.

En esta sección se presentará el video de MarketGo para mostrar la propuesta de valor, el recorrido por la landing page y las funciones principales de la aplicación web para administradores de minimarkets y proveedores. El enlace y la evidencia del video se incorporarán cuando esté disponible.
