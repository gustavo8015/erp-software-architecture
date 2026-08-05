# Proyecto ERP - Grupo X — Arquitectura de Software

Taller de arquitectura de software: gestión ágil del backlog (Notion) y documentación de arquitectura con **arc42**, **C4** y **PlantUML** para un Sistema ERP con módulos de Compras, Facturación, Stock/Costos, Activos Fijos, Empleados y EIS.

## Contenido del repositorio

| Carpeta / Archivo | Descripción |
|---|---|
| [`docs/arc42/`](docs/arc42/) | Documentación de arquitectura (plantilla arc42 en Markdown). |
| [`docs/images/`](docs/images/) | Diagramas exportados desde PlantUML (C1, C2, secuencia, MER). |
| [`docs/backlog/BACKLOG_NOTION.md`](docs/backlog/BACKLOG_NOTION.md) | Épicas, historias de usuario, criterios de aceptación y priorización MoSCoW. |
| [`diagrams/`](diagrams/) | Código fuente PlantUML (`.puml`) de todos los diagramas. |

## Documentos clave

- [1. Introducción y Objetivos](docs/arc42/01_introduction_and_goals.md)
- [2. Restricciones de Arquitectura](docs/arc42/02_architecture_constraints.md)
- [3. Alcance y Contexto (Diagrama C1)](docs/arc42/03_system_scope_and_context.md)
- [5. Vista de Bloques (Diagrama C2)](docs/arc42/05_building_block_view.md)
- [6. Vista de Ejecución (Secuencia + MER)](docs/arc42/06_runtime_view.md)
- [7. Vista de Despliegue](docs/arc42/07_deployment_view.md)
- [10. Glosario](docs/arc42/10_glossary.md)

## Stack tecnológico decidido

- **Backend:** Java 17 + Spring Boot (API monolítica REST)
- **Frontend:** SPA con React
- **Base de datos:** PostgreSQL
- **Diagramas:** PlantUML (modelo C4 + UML)

## Backlog

El Product Backlog se gestiona en Notion: **[enlace al tablero de Notion — reemplazar aquí]**.
