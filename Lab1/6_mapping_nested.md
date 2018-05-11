### Some words here

##### To-Do

Para crear documentos anidados se utiliza el tipo de campo `nested`

1. Modifica el índice 'coches' y crea un no nuevo que contenta los los campos `nombre` y `apellidos` anidados en un campo denominado `propietarios` ver tabla adjunta:

| Campo        | Tipo      | Formato    |
|--------------|-----------|------------|
| descripcion  | text      |            |
| fecha_compra | date      | dd-MM-yyyy |
| marca        | text      |            |
| pais         | text      |            |
| modelo       | text      |            |
| precio       | float     |            |
| location     | geo_point |            |
| propietarios | nested    |            |
| nombre       | text      |            |
| apellidos    | text      |            |


