# Diseño de la Base de Datos

## Tabla: usuarios

| Campo | Tipo | Descripción |
|---|---|---|
| id_usuario | INT | Identificador del usuario |
| nombre | VARCHAR | Nombre del usuario |
| correo | VARCHAR | Correo electrónico |
| password | VARCHAR | Contraseña |
| rol | VARCHAR | Rol del usuario |

## Tabla: categorias

| Campo | Tipo | Descripción |
|---|---|---|
| id_categoria | INT | Identificador de la categoría |
| nombre | VARCHAR | Nombre de la categoría |

## Tabla: productos

| Campo | Tipo | Descripción |
|---|---|---|
| id_producto | INT | Identificador del producto |
| id_categoria | INT | Categoría del producto |
| nombre | VARCHAR | Nombre de la comida |
| descripcion | VARCHAR | Descripción del producto |
| precio | DECIMAL | Precio del producto |
| imagen | VARCHAR | Imagen del producto |

## Tabla: pedidos

| Campo | Tipo | Descripción |
|---|---|---|
| id_pedido | INT | Identificador del pedido |
| id_usuario | INT | Usuario que realizó el pedido |
| fecha | DATETIME | Fecha y hora del pedido |
| estado | VARCHAR | Estado actual del pedido |
| total | DECIMAL | Total del pedido |

## Tabla: detalle_pedido

| Campo | Tipo | Descripción |
|---|---|---|
| id_detalle | INT | Identificador del detalle |
| id_pedido | INT | Pedido relacionado |
| id_producto | INT | Producto solicitado |
| cantidad | INT | Cantidad solicitada |
| precio | DECIMAL | Precio del producto |
| subtotal | DECIMAL | Subtotal |

## Relaciones

- Un usuario puede realizar varios pedidos.
- Un pedido puede contener varios productos.
- Un producto puede pertenecer a una categoría.
- Un pedido tiene varios detalles de pedido.
