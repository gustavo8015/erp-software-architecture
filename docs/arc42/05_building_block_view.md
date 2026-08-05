# 5. Vista de Bloques de Construcción

## 5.1 Diagrama de Contenedores (C4 — Nivel 2)

Se eligió una **arquitectura monolítica** por su simplicidad para la fase inicial del proyecto:

![Diagrama de Contenedores](../images/c2_containers.png)

## 5.2 Responsabilidades de los contenedores

| Contenedor | Tecnología | Responsabilidad |
|---|---|---|
| Single-Page Application | JavaScript, React | Interfaz de usuario en el navegador: formularios de productos, proveedores y órdenes de compra; validaciones básicas de entrada. |
| API Monolítica | Java, Spring Boot | Toda la lógica de negocio de los módulos del ERP: validaciones, reglas de compras, actualización de stock, integración con el sistema contable. |
| Base de Datos | PostgreSQL | Persistencia de todos los datos del ERP: productos, proveedores, órdenes, facturas, activos, empleados. |

## 5.3 Decisión de arquitectura

Se descartó microservicios en esta fase: el equipo es pequeño, el dominio aún se está descubriendo y un monolito modular (paquetes por módulo dentro de la API) reduce la complejidad operativa. Si un módulo crece (p. ej. Facturación), podrá extraerse como servicio independiente más adelante.
