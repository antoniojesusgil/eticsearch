
### Some words here
Para poder modificar índices, previamente hay que eliminarlos. Uso verbo `DELETE` y `PUT`

##### To-Do

1. Borra el índice `coches`

2. Crea un indice llamado `coches`. Los campos, tipo de dato y formato se detallan en la tabla.

| Campo        | Tipo      | Formato    |
|--------------|-----------|------------|
| descripcion  | text      |            |
| fecha_compra | date      | dd-MM-yyyy |
| marca        | keyword   |            |
| pais         | text      |            |
| modelo       | keyword   |            |
| precio       | float     |            |
| location     | geo_point |            |
