# 2. Restricciones de Arquitectura

## 2.1 Restricciones técnicas

| Restricción | Descripción |
|---|---|
| Backend | Java 17 con **Spring Boot** (API monolítica REST). |
| Frontend | **SPA con React** (JavaScript), comunicación vía HTTPS/JSON. |
| Base de datos | **PostgreSQL** como única base de datos relacional. |
| Diagramas | Toda la arquitectura se documenta con **PlantUML** (modelo C4 + UML). |
| Documentación | Plantilla **arc42** en Markdown, versionada en GitHub. |

## 2.2 Restricciones organizativas

| Restricción | Descripción |
|---|---|
| Gestión ágil | Product Backlog y Sprints gestionados en Notion (tablero "Proyecto ERP - Grupo X"). |
| Control de versiones | Repositorio público en GitHub: `erp-software-architecture`. |
| Alcance del taller | Se implementa la documentación de arquitectura; el código llegará en fases posteriores. |

## 2.3 Convenciones

- Historias de usuario en formato `Como <rol>, quiero <acción>, para que <beneficio>`.
- Criterios de aceptación en formato `Dado-Cuando-Entonces`.
- Priorización con **MoSCoW**.
