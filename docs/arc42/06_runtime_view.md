# 6. Vista de Ejecución

## 6.1 Escenario: Registrar un nuevo producto (HU-01)

Escenario crítico del Módulo de Compras: el gestor de inventario registra un producto nuevo en el catálogo.

![Diagrama de Secuencia - Registrar Producto](../images/sequence_registrar_producto.png)

**Flujo principal:**

1. El gestor de inventario diligencia el formulario de nuevo producto en la SPA.
2. La SPA valida campos obligatorios en el cliente y envía `POST /api/productos` con nombre, descripción y unidad de medida.
3. La API valida reglas de negocio (datos completos, duplicados por nombre).
4. La API inserta el registro en PostgreSQL (`INSERT INTO productos`).
5. La base de datos retorna el producto creado con su ID.
6. La API responde `201 Created` con el producto.
7. La SPA muestra mensaje de éxito y actualiza la lista de productos.

**Flujo alternativo:** si el nombre está vacío, la SPA muestra el error de validación sin llamar a la API.

## 6.2 Modelo de datos del Módulo de Compras (MER)

![MER Módulo de Compras](../images/mer_compras.png)

Entidades: `Producto`, `Proveedor`, `Producto_Proveedor` (relación N:M con precio), `Orden_Compra`, `Detalle_Orden_Compra` y `Recepcion_Mercancia`.
