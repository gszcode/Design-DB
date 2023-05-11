# Ventas

## Listado de Entidades

### clientes

- cliente_id **(PK)**
- nombre
- apellido
- telefono
- email
- direccion
- cp
- ciudad
- pais **(FK)**

### productos **(ED|EC)**

- producto_id **(PF)**
- nombre
- descripcion
- foto
- precio
- cantidad

### ventas **(ED)**

- venta_id **(PK)**
- cliente_id **(FK)**
- fecha
- monto

### articulos_x_venta

- articulo_id **(PK)**
- venta_id **(FK)**
- producto_id **(FK)**
- cantidad

### paises **(EC)**

- pais_id **(PK)**
- nombre
- dominio

# Relaciones

1. Un **cliente** tiene **pais** (_1 - 1_).
1. Un **cliente** genera **venta** (_1 - M_).
1. Una **venta** tiene **articulo** (_1 - M_).
1. Un **articulo** es un **producto** (_1 - 1_).
