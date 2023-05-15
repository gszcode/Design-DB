# GabyGram

## Listado de Entidades

### posts **(ED)**

- post_id **(PK)**
- post_date
- plot
- photo
- user **(FK)**

### users **(ED)**

- user_id **(PK)**
- user_date
- username
- email **(UQ)**
- password
- phone **(UQ)**
- bio
- web
- avatar
- birthdate
- genre
- country **(FK)**

### comments **(ED | EP)**

- comment_id **(PK)**
- comment_date
- comment
- post_id **(FK)**
- user **(FK)**

### hearts **(ED | EP)**

- hear_id **(PK)**
- heart_date
- post_id **(FK)**
- user **(FK)**

### follows **(ED)**

- follow_id **(PK)**
- follow_date
- follow_user **(FK)**
- followin_user **(FK)**

### countries **(EC)**

- country_id **(PK)**
- country_name

## Relaciones

1. Un **User** publica **posts** (_1 - M_).
1. Un **User** pertenece a **country** (_1 - 1_).
1. Un **Post** tiene **comments** (_1 - M_).
1. Un **User** hace **comments** (_1 - M_).
1. Un **Post** contiene **hearts** (_1 - M_).
1. Un **User** da un **heart** (_1 - 1_).
1. Un **User** sigue **follows** (_1 - M_).
1. Un **User** recibe **follows** (_1 - M_).

## Diagramas

### Modelo Relacional de la BD

![Modelo Relacional](GabyGram_ModeloRelacionalBD.png)

## Reglas de Negocio

### posts

1. Crear un post
1. Leer todos los post
1. Leer un post en particular
1. Leer los post de un user
1. Actualizar el plot de un post
1. Eliminar un post

### users

1. Crear un user
1. Leer todos los users
1. Leer un user en particular
1. Validar un user
1. Actualizar datos de un user
1. Actualizar password de un user
1. Eliminar un user

### comments

1. Crear un comment en un post
1. Leer todos los comments de un post
1. Leer un comment de un post
1. Contar el numero de comments en un post
1. Eliminar comment de un post

### hearts

1. Crear heart de user en un post
1. Leer el numero de hearts de un post
1. Eliminar heart de user en un post

### follows

1. Crear un follow de un user
1. Contar el numero de followers de un user
1. Contar el numero de followings de un user
1. Eliminar follow de un user

### countries

1. Crear country
1. Leer todos los countries
1. Leer un country
1. Actualizar un country
1. Eliminar country
