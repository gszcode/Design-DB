# EA$Y

## Listado de Entidades

### usuarios **(ED)**

- usuario_id **(PK)**
- nombre
- apellido
- telefono **(UQ)**
- email **(UQ)**
- contraseña
- direccion
- cp
- ciudad
- pais **(FK)**

### transferencias **(ED)**

- transferencia_id **(PK)**
- medio_de_transferencia **(FK)**
- usuario_destino **(FK)**
- monto
- motivo
- fecha
- estado

### pagos **(ED)**

- pago_id **(PK)**
- medio_de_transferencia **(FK)**
- destino
- monto
- motivo
- fecha
- estado

### depositos_a_cuenta **(ED)**

- deposito_id **(PK)**
- medio_de_transferencia **(FK)**
- monto
- fecha
- estado

### opciones_de_transferencias **(EC)**

- opcion_id **(PK)**
- nombre

### paises **(EC)**

- pais_id **(PK)**
- nombre
- dominio **(UQ)**

# Relaciones

1. Un **usuario** tiene **pais** (_1 - 1_)
1. Un **usuario** hace **transferencia** (_1 - M_)
1. Un **usuario** hace **pago** (_1 - M_)
1. Un **usuario** hace **deposito** (_1 - M_)
1. Una **transferencia** pertenece **usuario** (_1 - 1_)
1. Un **pago** pertenece **usuario** (_1 - 1_)
1. Un **deposito** pertenece **usuario** (_1 - 1_)
