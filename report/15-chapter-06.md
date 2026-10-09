# Conclusiones

## Conclusiones y recomendaciones.

**Conclusiones***

1. El análisis del Capítulo I permitió identificar que la gestión de productos orgánicos en minimarkets presenta una problemática real y medible: las pérdidas alimentarias en el Perú alcanzan el 47,6% de la oferta anual, y se agravan por el uso de procesos manuales y herramientas fragmentadas (hojas de cálculo, libretas y mensajería). Mediante la técnica 5W+2H y el análisis competitivo, concluimos que FreshTracker, ShelfLife y Peru Marketplace cubren solo una parte del proceso (conservación, inventario o conexión B2B).

2. La aplicación del proceso Lean UX (Problem Statement, Assumptions, Hypothesis Statements y Canvas) permitió traducir supuestos de negocio en nueve hipótesis verificables, cada una vinculada de forma trazable a un Business Outcome, un User Outcome y un Feature Assumption.

3. El análisis de los dos segmentos objetivo (administradores de minimarkets y proveedores), sus personas (Russell Estrada y Marco Antonio Ríos) y sus restricciones llevó a decisiones técnicas clave. Optamos por una arquitectura de plataforma web responsive con Landing Page, Web Application y RESTful API, con una infraestructura compartida pero con dashboards, roles y permisos diferenciados por segmento.

4. El análisis competitivo mostró que FreshTracker, ShelfLife y Peru Marketplace resuelven solo una parte del proceso. MarketGo se diferencia al integrar inventario, conservación y abastecimiento. Las personas (Russell y Marco Antonio), la User Task Matrix y los Journey Maps mostraron que los puntos críticos son la transcripción manual de pedidos y la falta de alertas. Por eso la plataforma debe ser responsive, con dashboards y permisos según el rol.

3. El Big Picture Event Storming y el Ubiquitous Language definieron un vocabulario común (lote, stock mínimo, solicitud, recepción, conservación) y permitieron identificar contextos como Inventory, Procurement, Conservation y Communication. Esto sienta las bases de una arquitectura basada en DDD, donde cada término del negocio tiene un único significado en documentación y código.

4. Las 33 User Stories, las Technical Stories y las Functional Stories se organizaron en 8 épicas. Cada una responde a un hallazgo de las entrevistas, como el control de lotes, las alertas y el seguimiento de pedidos. El Impact Mapping las vinculó con dos objetivos SMART: reducir 30% las mermas y bajar de 24 h a menos de 4 h el tiempo entre pedido y orden de envío. Aprendimos que cada requisito debe poder justificarse con un objetivo de negocio medible.

5. El Product Backlog priorizó 63 ítems con Story Points, y la matriz de endpoints REST (/api/v1/...) conecta cada contrato con su historia de origen. Las mejoras de backend (ASP.NET Core, EF Core, migraciones, Swagger) permiten avanzar con una API documentada y persistencia real. Aprendimos que definir los contratos antes de programar facilita la coordinación entre frontend y backend.

6. Se definió una guía de estilo con paleta (azules, naranja de acento y neutros), tipografía Arimo, espaciado, iconografía Tabler y rejilla responsive. Con ello, el landing y la aplicación comparten una misma identidad. La arquitectura de información (sidebar con cuatro grupos, etiquetas cortas, estados con color y navegación según el rol) se validó con wireframes, mock-ups, wireflows y user flows. Aprendimos que diseñar con base en las tareas reales de Russell y Marco reduce la complejidad de la interfaz.

7. El Design-Level EventStorming permitió identificar 12 bounded contexts (IAM, Profiles, Inventory, Requisition, Procurements, Conservation, Communication, entre otros). Estos se reflejaron en los diagramas C4 (contexto, contenedores y componentes), con una Landing Page, una SPA, una API REST y una base de datos. Esta separación mantiene las responsabilidades del negocio aisladas y facilita que el equipo trabaje en paralelo.

8. Se configuró un entorno común con GitHub, GitFlow (main, develop, feature y hotfix), Pull Requests y Conventional Commits. También se definieron guías de estilo por lenguaje (Vue, C#, HTML/CSS, Gherkin) y convenciones de nomenclatura en inglés alineadas al Ubiquitous Language. Aprendimos que acordar estas reglas desde el inicio facilita la trazabilidad y reduce conflictos cuando cinco personas trabajan en paralelo.

9. El Sprint 1 cumplió su objetivo: se implementó la landing page con las secciones Home, Producto, Videos, Planes y Contacto. Las siete tareas planificadas (14 Story Points) quedaron en Done. Esto demostró que dividir el trabajo por secciones y por aspectos (diseño, estructura Vue, contenido y despliegue) permite avanzar sin bloqueos y mostrar valor desde el primer sprint.}

10. La landing page se desplegó en Azure Static Web Apps, y el avance quedó respaldado por el historial de commits, el tablero del sprint y capturas de ejecución. Publicar desde el primer sprint permite validar el producto con usuarios reales y deja una base de despliegue lista para los sprints siguientes, donde se integrarán el frontend, el backend en .NET y la persistencia.

**Recomendaciones**

1. Definir una Definition of Done común. En el Sprint 1 cada integrante interpretó "terminado" a su manera. Recomendamos acordar por escrito qué significa Done: código revisado mediante PR, responsive verificado, textos en i18n y despliegue comprobado.
Proteger las ramas main y develop. Activar en GitHub la revisión obligatoria de al menos una persona y bloquear los pushes directos, para que GitFlow no dependa solo de la disciplina del equipo.

2. Vincular siempre las tareas con las User Stories del Product Backlog. Cada tarea del sprint debe referenciar un ID real (por ejemplo US-031), de modo que la trazabilidad entre requisito, tarea, commit y evidencia sea completa.
Usar una sola herramienta de gestión. Mantener Trello como fuente única para backlog y sprint, y que las capturas de la documentación salgan siempre de esa herramienta.

3. Mantener una sola terminología. Usar los mismos términos del Ubiquitous Language en la documentación, el código y la interfaz: "pedido" (requisitions) y "orden de envío" (purchase-orders), y el nombre del equipo "Market-Labs".
Automatizar la integración y el despliegue. Configurar GitHub Actions para ejecutar lint y build en cada PR, y para desplegar automáticamente a Azure al integrar en main.

4. Escribir pruebas desde el inicio. Convertir los escenarios Gherkin de las User Stories en pruebas automatizadas, empezando por las reglas críticas: solo el administrador modifica el inventario y la aceptación de una orden de envío no puede aplicarse dos veces.

5. Validar con usuarios reales. Compartir la landing page con los administradores y proveedores entrevistados en el Capítulo II y medir si entienden la propuesta de valor y si completan el formulario de contacto.