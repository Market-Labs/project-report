# Conclusiones

## Conclusiones y recomendaciones.

**Conclusiones**

1. El análisis del Capítulo I permitió identificar que la gestión de productos orgánicos en minimarkets presenta una problemática real y medible: las pérdidas alimentarias en el Perú alcanzan el 47,6% de la oferta anual, y se agravan por el uso de procesos manuales y herramientas fragmentadas (hojas de cálculo, libretas y mensajería). Mediante la técnica 5W+2H y el análisis competitivo, concluimos que FreshTracker, ShelfLife y Peru Marketplace cubren solo una parte del proceso (conservación, inventario o conexión B2B).

2. La aplicación del proceso Lean UX (Problem Statement, Assumptions, Hypothesis Statements y Canvas) permitió traducir supuestos de negocio en nueve hipótesis verificables, cada una vinculada de forma trazable a un Business Outcome, un User Outcome y un Feature Assumption.

3. El análisis de los dos segmentos objetivo (administradores de minimarkets y proveedores), sus personas (Russell Estrada y Marco Antonio Ríos) y sus restricciones llevó a decisiones técnicas clave. Optamos por una arquitectura de plataforma web responsive con Landing Page, Web Application y RESTful API, con una infraestructura compartida pero con dashboards, roles y permisos diferenciados por segmento.

4. El análisis competitivo mostró que FreshTracker, ShelfLife y Peru Marketplace resuelven solo una parte del proceso. MarketGo se diferencia al integrar inventario, conservación y abastecimiento. Las personas (Russell y Marco Antonio), la User Task Matrix y los Journey Maps mostraron que los puntos críticos son la transcripción manual de pedidos y la falta de alertas. Por eso la plataforma debe ser responsive, con dashboards y permisos según el rol.

5. El Big Picture Event Storming y el Ubiquitous Language definieron un vocabulario común (lote, stock mínimo, solicitud, recepción, conservación) y permitieron identificar contextos como Inventory, Procurement, Conservation y Communication. Esto sienta las bases de una arquitectura basada en DDD, donde cada término del negocio tiene un único significado en documentación y código.

6. Las 33 User Stories, las Technical Stories y las Functional Stories se organizaron en 8 épicas. Cada una responde a un hallazgo de las entrevistas, como el control de lotes, las alertas y el seguimiento de pedidos. El Impact Mapping las vinculó con dos objetivos SMART: reducir 30% las mermas y bajar de 24 h a menos de 4 h el tiempo entre pedido y orden de envío. Aprendimos que cada requisito debe poder justificarse con un objetivo de negocio medible.

7. El Product Backlog ayudó a relacionar las historias con los servicios que necesitaba la aplicación. En el Sprint 3 avanzamos con una API en ASP.NET Core, persistencia en MySQL y documentación en Swagger. Las pruebas locales de registro y proveedores mostraron que acordar los datos entre frontend y backend antes de integrarlos evita confusiones y retrabajo.

8. Se definió una guía de estilo con paleta (azules, naranja de acento y neutros), tipografía Arimo, espaciado, iconografía Tabler y rejilla responsive. Con ello, el landing y la aplicación comparten una misma identidad. La arquitectura de información (sidebar con cuatro grupos, etiquetas cortas, estados con color y navegación según el rol) se validó con wireframes, mock-ups, wireflows y user flows. Aprendimos que diseñar con base en las tareas reales de Russell y Marco reduce la complejidad de la interfaz.

9. El Design-Level EventStorming permitió identificar 12 bounded contexts (IAM, Profiles, Inventory, Requisition, Procurements, Conservation, Communication, entre otros). Estos se reflejaron en los diagramas C4 (contexto, contenedores y componentes), con una Landing Page, una SPA, una API REST y una base de datos. Esta separación mantiene las responsabilidades del negocio aisladas y facilita que el equipo trabaje en paralelo.

10. Se configuró un entorno común con GitHub, GitFlow (main, develop, feature y hotfix), Pull Requests y Conventional Commits. También se definieron guías de estilo por lenguaje (Vue, C#, HTML/CSS, Gherkin) y convenciones de nomenclatura en inglés alineadas al Ubiquitous Language. Aprendimos que acordar estas reglas desde el inicio facilita la trazabilidad y reduce conflictos cuando cinco personas trabajan en paralelo.

11. El Sprint 1 cumplió su objetivo: se implementó la landing page con las secciones Home, Producto, Videos, Planes y Contacto. Las siete tareas planificadas (14 Story Points) quedaron en Done. Esto demostró que dividir el trabajo por secciones y por aspectos (diseño, estructura Vue, contenido y despliegue) permite avanzar sin bloqueos y mostrar valor desde el primer sprint.

12. La landing page se publicó primero en Azure Static Web Apps y después pasó a Vercel, donde también se aloja el frontend actual. Tener ambas páginas disponibles permitió mostrar el producto y facilitar el acceso a la aplicación durante las entrevistas de validación.

13. En el Sprint 2 desarrollamos la primera versión navegable del frontend con Vue 3, Vite, Pinia y PrimeVue. Las vistas para administradores de minimarkets y proveedores organizaron funciones de inventario, productos, abastecimiento y pedidos según el rol. Este trabajo nos ayudó a convertir el diseño del capítulo IV en pantallas que los usuarios pudieron recorrer y comentar.

14. En el Sprint 3 se implementaron servicios del backend para los módulos de MarketGo y se preparó la base de datos MySQL. Swagger permitió revisar las rutas y comprobar en local el registro de usuarios y la creación de proveedores. El panel de Vercel muestra el despliegue del backend; estas evidencias nos ayudaron a pasar de una aplicación de demostración a una integración con servicios propios.

15. Al registrar una cuenta nueva de minimarket, el dashboard del frontend mostró correctamente el estado inicial sin productos, solicitudes ni envíos. Esta prueba fue útil porque confirmó que la interfaz puede presentar datos de una cuenta recién creada sin inventar actividad. Todavía conviene revisar los flujos completos entre módulos para que la experiencia sea consistente en todos los casos.

16. Las entrevistas de validación y la evaluación heurística nos dieron una mirada distinta a la del equipo de desarrollo. Los usuarios valoraron tener inventario y pedidos en un mismo lugar, pero también señalaron dudas sobre los planes, la disponibilidad de productos y algunos mensajes de la interfaz. Estos hallazgos nos sirven para priorizar mejoras concretas en vez de guiarnos solo por nuestras propias suposiciones.

**Recomendaciones**

1. Definir una Definition of Done común. En el Sprint 1 cada integrante interpretó "terminado" a su manera. Recomendamos acordar por escrito qué significa Done: código revisado mediante PR, responsive verificado, textos en i18n y despliegue comprobado.

2. Proteger las ramas main y develop. Activar en GitHub la revisión obligatoria de al menos una persona y bloquear los pushes directos, para que GitFlow no dependa solo de la disciplina del equipo.

3. Vincular siempre las tareas con las User Stories del Product Backlog. Cada tarea del sprint debe referenciar un ID real (por ejemplo US-031), de modo que la trazabilidad entre requisito, tarea, commit y evidencia sea completa.

4. Usar una sola herramienta de gestión. Mantener Trello como fuente única para backlog y sprint, y que las capturas de la documentación salgan siempre de esa herramienta.

5. Mantener una sola terminología. Usar los mismos términos del Ubiquitous Language en la documentación, el código y la interfaz: "pedido" (requisitions) y "orden de envío" (purchase-orders), y el nombre del equipo "Market-Labs".

6. Automatizar las verificaciones antes de desplegar. Conviene ejecutar la compilación y las pruebas del frontend y del backend en cada cambio importante, y comprobar que las versiones publicadas en Vercel correspondan al código revisado.

7. Probar los flujos completos entre frontend, API y base de datos. Empezar por registro e inicio de sesión, creación de proveedores, inventario y seguimiento de pedidos, incluyendo los permisos de cada rol y los mensajes cuando ocurre un error.

8. Aplicar las mejoras encontradas en las entrevistas y la evaluación heurística. Aclarar las diferencias entre planes, facilitar el filtro de productos disponibles, advertir cuando una solicitud supera el stock y unificar las fechas y mensajes que ve cada usuario.