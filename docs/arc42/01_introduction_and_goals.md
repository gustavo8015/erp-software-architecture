# 1. Introducción y Objetivos

## 1.1 Objetivo del sistema

El **Sistema ERP** integra los procesos de negocio de la empresa en una sola plataforma: Compras, Facturación, Stock/Costos, Activos Fijos, Empleados y EIS (información ejecutiva). Este documento se centra en la arquitectura inicial, con énfasis en el **Módulo de Compras**.

## 1.2 Requisitos de negocio principales (Módulo de Compras)

- Registrar y mantener el catálogo de **productos** (nombre, descripción, unidad de medida).
- Registrar **proveedores** con razón social, NIT y datos de contacto.
- Asociar productos a proveedores con **precio unitario** y tiempo de entrega.
- Crear y gestionar **órdenes de compra** con detalle de productos y cantidades.
- Registrar la **recepción de mercancía** y actualizar el stock.
- Consultar el **historial de compras** con filtros por proveedor, fecha y estado.

## 1.3 Objetivos de calidad

| Prioridad | Objetivo | Motivación |
|---|---|---|
| 1 | Integridad de datos | Las compras alimentan stock, costos y contabilidad; los datos deben ser consistentes. |
| 2 | Usabilidad | Los usuarios administrativos deben operar sin capacitación extensa. |
| 3 | Mantenibilidad | El ERP crecerá módulo a módulo; el código debe ser fácil de extender. |

## 1.4 Partes interesadas

| Rol | Expectativa |
|---|---|
| Administrador de Compras | Gestionar proveedores y órdenes de compra de forma ágil. |
| Gestor de Inventario | Catálogo de productos actualizado y stock confiable. |
| Gerencia | Indicadores de compras y costos en el módulo EIS. |
| Equipo de desarrollo | Documentación de arquitectura clara (arc42 + C4). |
