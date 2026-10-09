# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management.

En esta sección se describen las decisiones, convenciones y principios adoptados por el equipo de **Market-Labs** para garantizar la coherencia, trazabilidad y control de versiones durante el ciclo de vida del desarrollo de la solución **MarketGo**. Se establecen los lineamientos para la configuración del entorno de desarrollo, gestión del código fuente, convenciones de estilo y configuración de despliegue orientada a la nube.

### 5.1.1. Software Development Environment Configuration.

Se especifican los productos de software utilizados durante el ciclo de vida del proyecto, organizados por disciplinas técnicas para asegurar la estandarización del entorno entre los desarrolladores de MarketGo.

#### Project Management
* **Trello:** Empleado para la organización visual del flujo de trabajo diario y la priorización rápida de tareas durante el desarrollo de los módulos de inventario y pedidos (Atlassian, s. f.).
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
| Proposed User Stories | US-027 Inicio de sesión (3 SP); US-002 Visualizar inventario (5 SP); US-017 Consultar productos ofrecidos (3 SP); US-019 Consultar pedidos de abastecimiento (3 SP). Esta selección propone un primer incremento navegable del frontend para ambos roles. |
| Sprint 2 Velocity | 14 Story Points, capacidad inicial estimada a partir de la velocidad registrada en Sprint 1. |
| Sum of Story Points | 14 Story Points (3 + 5 + 3 + 3) para las historias propuestas. |

**Repositorio Landing Page:** https://github.com/Market-Labs/landign-page.git
**Repositorio Frontend:** https://github.com/Market-Labs/front-end.git

#### 5.2.2.2. Aspect Leaders and Collaborators.

Para el Sprint 2 se identificaron aspectos funcionales que corresponden a los bounded contexts implementados en el frontend, más un aspecto transversal de Project Setup (Vue 3 + Vite + Pinia + i18n + json-server) y un aspecto para la versión v2 del Landing Page. La siguiente matriz LACX identifica los aspectos principales del Sprint y asigna responsabilidades (Líder/Colaborador) al equipo de Market-labs, alineadas con las fortalezas técnicas evidenciadas durante el Sprint 1.

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
  <img src="docs/assets/chapter-05/jira2.png" alt="Sprint 2 Board Screenshot" width="100%">
  <p><em>Figura: Tablero del Sprint 2 en Trello (Proyecto MarketGo)</em></p>
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


#### 5.2.2.4. Development Evidence for Sprint Review.


<p>
  Resumen de los commits más relevantes correspondientes a las mejoras
  solicitadas por el docente para la Landing Page de
  <strong>MarketGo</strong>, producto desarrollado por
  <strong>MarketLab</strong>. Las mejoras incluyen la adaptación de
  las Historias de Usuario al rol Visitante (Visitor) y la incorporación
  de enlaces interactivos a redes sociales (LinkedIn, X y Facebook).
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
      <td>refactor(landing): improve visitor experience based on instructor feedback</td>
      <td>19-09-2026</td>
    </tr>
    <tr>
      <td>feature/contact-section</td>
      <td><code>a6446e1</code></td>
      <td>feat(contact): add LinkedIn, X and Facebook social media links</td>
      <td>19-09-2026</td>
    </tr>
    <tr>
      <td>feature/contact-section</td>
      <td><code>fbf450a</code></td>
      <td>fix(contact): enable interactive social media icons and external navigation</td>
      <td>19-09-2026</td>
    </tr>
    <tr>
      <td>develop</td>
      <td><code>1f850de</code></td>
      <td>fix(landing): align visitor interactions with rubric requirements</td>
      <td>19-09-2026</td>
    </tr>
    <tr>
      <td>main</td>
      <td><code>1f850de</code></td>
      <td>fix(landing): align visitor interactions with rubric requirements</td>
      <td>19-09-2026</td>
    </tr>
  </tbody>
</table>


#### 5.2.2.5. Execution Evidence for Sprint Review.

<p>
  Al cierre del Sprint 2, el equipo de MarketLab presentó los avances
  funcionales del Frontend Web Application de <strong>MarketGo</strong>,
  una plataforma orientada a la gestión de inventarios, productos,
  abastecimiento y conservación de productos orgánicos en minimarkets.
  La aplicación fue desarrollada utilizando Angular y organizada
  mediante componentes, servicios y bounded contexts, con interfaces
  diferenciadas para los roles de Administrador de Minimarket y
  Proveedor. El alcance funcional trabajado durante el Sprint 2
  comprende los siguientes flujos:
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
</ul>

<p>
  La aplicación contempla soporte de internacionalización
  <strong>i18n</strong> (español e inglés), una interfaz basada
  en Angular y navegación mediante Angular Router. Asimismo,
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
  <img src="docs/assets/chapter-05/sprint2-signin.png" alt="Sign-In View" width="90%">
  <p><em>Figura: Vista de inicio de sesión del bounded context IAM de MarketGo.</em></p>
</div>

<div align="center">
  <img src="docs/assets/chapter-05/sprint2-requisitions.png" alt="Supply Requests View" width="90%">
  <p><em>Figura: Gestión de pedidos de abastecimiento realizados por administradores de minimarkets.</em></p>
</div>

<div align="center">
  <img src="docs/assets/chapter-05/sprint2-suppliers.png" alt="Supplier Directory" width="90%">
  <p><em>Figura: Directorio de proveedores orgánicos y catálogo de productos disponibles para abastecimiento.</em></p>
</div>

<div align="center">
  <img src="docs/assets/chapter-05/sprint2-procurement.png" alt="Supply Orders Management" width="90%">
  <p><em>Figura: Gestión de pedidos de abastecimiento y órdenes de envío entre proveedores y administradores.</em></p>
</div>

<div align="center">
  <img src="docs/assets/chapter-05/sprint2-inventory.png" alt="Inventory Management" width="90%">
  <p><em>Figura: Visualización del inventario con información de productos, lotes, existencias y fechas de vencimiento.</em></p>
</div>

<div align="center">
  <img src="docs/assets/chapter-05/sprint2-dashboard.png" alt="MarketGo Dashboard" width="90%">
  <p><em>Figura: Dashboard general de MarketGo con indicadores operativos diferenciados según el rol del usuario.</em></p>
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
  <a href="URL_DEL_VIDEO_DE_MARKETGO" target="_blank">
    <img src="docs/assets/chapter-05/video-screenshot.png" alt="Video Demostrativo MarketGo en Microsoft Stream" width="90%" style="border: 1px solid #ccc; border-radius: 8px;">
  </a>
  <p><em>Figura: Video demostrativo de navegación de MarketGo en Microsoft Stream.</em></p>
</div>

Enlace directo: URL_DEL_VIDEO_DE_MARKETGO

#### 5.2.2.6. Services Documentation Evidence for Sprint Review.

#### 5.2.2.7. Software Deployment Evidence for Sprint Review.

#### 5.2.2.8. Team Collaboration Insights during Sprint.
