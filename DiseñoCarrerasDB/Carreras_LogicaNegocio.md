# Carreras

## Listado de Entidades

### carreras **(ED)**

- carrera_id **(PK)**
- nombre
- tipo_carrera **(FK)**
- fecha
- tiempo
- mejor_tiempo
- altitud
- lugar
- pais **(FK)**
- foto

### tipos_carrera **(EC)**

- tipo_carrera **(PK)**
- descripcion
- distancia **(UQ)**

### paises **(EC)**

- pais_id **(PK)**
- nombre

## Relaciones

1. Una **carrera** _pertenece_ a un **tipo de carrera**. (_1 a 1_)
1. Una **carrera** se _corre_ en un **país**. (_1 a 1_)

## Diagramas

### Modelo Entidad - Relación

![Modelo Entidad - Relacion](./CarrerasModeloE-R.png)

### Modelo Relacional De la BD

![Modelo Entidad - Relacion](./CarrerasModeloRelacionalBD.png)

## Reglas de Negocio

### carreras **(ED)**

1. Todos los valores del atributo distancia, deberán estar expresados en _km_ y no se podrán repetir.
1. Crear el registro de una carrera.
1. Leer el registro de una(s) carrera(s) dada una condición en particular.
1. Leer todos los registro de la entidad carreras.
1. Actualizar los datos de una carrera dada una condición en particular.
1. Eliminar los datos de una carrera dada una condición en particular.

### tipos_carrera **(EC)**

1. Crear el registro de un tipo carrera.
1. Leer el registro de un(os) tipo(s) de carrera(s) dada una condición en particular.
1. Leer todos los registro de la entidad tipos de carreras.
1. Actualizar los datos de un tipo de carrera dada una condición en particular.
1. Eliminar los datos de un tipo de carrera dada una condición en particular.

### paises **(EC)**

1. Crear el registro de un país.
1. Leer el registro de un(os) pais(es) dada una condición en particular.
1. Leer todos los registro de la entidad paises.
1. Actualizar los datos de un país dada una condición en particular.
1. Eliminar los datos de un país dada una condición en particular.
