# Product Backlog — Proyecto ERP - Grupo X

> Contenido listo para copiar en Notion. Estructura sugerida: una base de datos "Backlog" con propiedades **Tipo** (Épica / Historia), **Épica** (relación), **Prioridad MoSCoW** (select) y **Estado** (select).

---

## Épicas

| Épica | Descripción |
|---|---|
| Módulo de Compras | Gestión de productos, proveedores y órdenes de compra. |
| Módulo de Facturación | Emisión y gestión de facturas de venta. |
| Módulo Stock/Costos | Control de inventario, movimientos y costeo. |
| Módulo Activos Fijos | Registro y depreciación de activos fijos. |
| Módulo Empleados | Gestión de información de empleados y nómina básica. |
| Módulo EIS | Indicadores y reportes ejecutivos para la dirección. |

---

## Historias de Usuario — Épica: Módulo de Compras

### HU-01 — Registrar nuevos productos — **Must have**
**Como** gestor de inventario, **quiero** registrar nuevos productos con su información básica (nombre, descripción, unidad de medida), **para que** pueda mantener un catálogo actualizado para las compras.

**Criterios de aceptación**
1. Dado que estoy en la pantalla de gestión de productos, cuando relleno el formulario con datos válidos y hago clic en "Guardar", entonces el nuevo producto debe aparecer en la lista de productos.
2. Dado que intento guardar un producto, cuando dejo el campo "nombre" vacío, entonces el sistema debe mostrar un mensaje de error y no guardar el producto.
3. Dado que registro un producto, cuando ya existe otro producto con el mismo nombre, entonces el sistema debe advertir el duplicado y pedir confirmación antes de guardar.

### HU-02 — Registrar proveedores — **Must have**
**Como** administrador de compras, **quiero** registrar proveedores con su razón social, NIT y datos de contacto, **para que** pueda asociarlos a los productos y emitirles órdenes de compra.

**Criterios de aceptación**
1. Dado que estoy en la pantalla de proveedores, cuando completo razón social, NIT y contacto válidos y guardo, entonces el proveedor aparece en el listado de proveedores.
2. Dado que registro un proveedor, cuando el NIT ya existe en el sistema, entonces se muestra un error de duplicado y no se crea el registro.
3. Dado que registro un proveedor, cuando el correo electrónico tiene formato inválido, entonces el sistema muestra un mensaje de error en el campo y no permite guardar.

### HU-03 — Asociar productos a proveedores con precio — **Should have**
**Como** administrador de compras, **quiero** asociar productos a uno o varios proveedores con su precio unitario y tiempo de entrega, **para que** pueda comparar condiciones al momento de comprar.

**Criterios de aceptación**
1. Dado que estoy en la ficha de un producto, cuando selecciono un proveedor e ingreso precio unitario válido y guardo, entonces la asociación aparece en la lista de proveedores del producto.
2. Dado que asocio un proveedor a un producto, cuando ingreso un precio unitario negativo o cero, entonces el sistema muestra un error y no guarda la asociación.
3. Dado que un producto tiene varios proveedores asociados, cuando consulto la ficha del producto, entonces veo la lista ordenada por precio unitario de menor a mayor.

### HU-04 — Crear órdenes de compra — **Must have**
**Como** administrador de compras, **quiero** crear órdenes de compra seleccionando proveedor, productos y cantidades, **para que** pueda formalizar las solicitudes de compra a los proveedores.

**Criterios de aceptación**
1. Dado que creo una orden de compra, cuando selecciono un proveedor, agrego al menos un producto con cantidad válida y guardo, entonces la orden se crea en estado "Emitida" con un número consecutivo.
2. Dado que creo una orden de compra, cuando intento guardarla sin líneas de detalle (sin productos), entonces el sistema muestra un error y no crea la orden.
3. Dado que agrego un producto a la orden, cuando el producto tiene precio registrado para el proveedor seleccionado, entonces el precio unitario se carga automáticamente y puede editarse.

### HU-05 — Registrar recepción de mercancía — **Should have**
**Como** gestor de inventario, **quiero** registrar la recepción de la mercancía asociada a una orden de compra, **para que** el stock se actualice y quede trazabilidad de lo recibido frente a lo pedido.

**Criterios de aceptación**
1. Dado que existe una orden de compra en estado "Emitida", cuando registro la recepción con cantidades recibidas válidas, entonces el stock de los productos se incrementa y la orden pasa a "Recibida" (total o parcial).
2. Dado que registro una recepción, cuando la cantidad recibida supera la cantidad pedida, entonces el sistema muestra una advertencia y exige confirmación con observación obligatoria.
3. Dado que una orden ya está en estado "Recibida total", cuando intento registrar una nueva recepción sobre ella, entonces el sistema lo impide y muestra un mensaje informativo.

### HU-06 — Consultar historial de compras — **Could have**
**Como** administrador de compras, **quiero** consultar el historial de órdenes de compra filtrando por proveedor, fecha y estado, **para que** pueda hacer seguimiento y auditoría de las compras.

**Criterios de aceptación**
1. Dado que estoy en el listado de órdenes, cuando aplico un filtro por proveedor y rango de fechas, entonces solo se muestran las órdenes que cumplen ambos criterios.
2. Dado que consulto una orden del historial, cuando abro su detalle, entonces veo proveedor, líneas de productos, cantidades, precios, estado y recepciones asociadas.
3. Dado que el listado tiene más de 20 resultados, cuando navego entre páginas, entonces los filtros aplicados se mantienen.

### HU-07 — Exportar catálogo de productos — **Won't have (esta versión)**
**Como** gestor de inventario, **quiero** exportar el catálogo de productos a Excel/CSV, **para que** pueda compartirlo con otras áreas. *(Se pospone para una versión futura.)*

---

## Resumen de priorización MoSCoW

| Historia | Prioridad |
|---|---|
| HU-01 Registrar productos | Must have |
| HU-02 Registrar proveedores | Must have |
| HU-04 Crear órdenes de compra | Must have |
| HU-03 Asociar productos-proveedores | Should have |
| HU-05 Recepción de mercancía | Should have |
| HU-06 Historial de compras | Could have |
| HU-07 Exportar catálogo | Won't have |

**Justificación:** sin productos (HU-01), proveedores (HU-02) y órdenes (HU-04) no existe proceso de compras; son el mínimo viable. HU-03 y HU-05 agregan valor operativo pero el proceso puede iniciar sin ellas. HU-06 es de conveniencia. HU-07 se descarta en esta versión por bajo valor relativo.
