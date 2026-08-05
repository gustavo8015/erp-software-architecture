# 3. Alcance y Contexto del Sistema

## 3.1 Contexto de negocio

El Sistema ERP es usado por el **Administrador de Compras**, el **Gestor de Inventario** y la **Gerencia**. Se integra con un **sistema contable externo** (asientos y facturas), con la **DIAN** para facturación electrónica y con los **proveedores** a quienes se envían las órdenes de compra.

## 3.2 Diagrama de Contexto (C4 — Nivel 1)

El sistema se muestra como una caja negra con sus usuarios y sistemas externos:

![Diagrama de Contexto](../images/c1_context.png)

| Elemento | Tipo | Interacción |
|---|---|---|
| Administrador de Compras | Persona | Registra productos, proveedores y órdenes de compra. |
| Gestor de Inventario | Persona | Consulta y actualiza catálogo y stock. |
| Gerente / Directivo | Persona | Consulta reportes e indicadores (EIS). |
| Sistema Contable Externo | Sistema externo | Recibe facturas y asientos contables. |
| DIAN / Facturación Electrónica | Sistema externo | Valida las facturas electrónicas emitidas. |
| Proveedores | Sistema externo | Reciben las órdenes de compra. |
