Ya has aprendido a utilizar logstash y a crear un index pattern en Kibana. Este ejercicio es de consolidación de los conocimientos.

### To-Do

Utiliza el fichero `pipeline2.conf` para construir el script

1. Borra el indice creado
2. Añade un nuevo campo denominado `markets` en función del dispositivo.
>Market obtiene dos valores, `Apple` o `Google`

3. Añade nuevo capo denominado `Pais_long` en funcion del pais.
	
| Pais    | Pais_long     |
| ------- |:-------------:|
| ES      | España        |
| IT      | Italia        |
| JP      | Japón         |
| NL      | Holanda       |
| GB      | Gran Bretaña  |
| DE      | Alemania      |
| US      | Estados Unidos|

4. Ejecuta logstash contra elasticsearch y crea un índice llamado `markets`.
>Para indicar a logstash que utilize el script hay que pasar el flag `-f`

7. Comprobar que se ha creado el índice, visualiza la consola.
8. Crear el index pattern en kibana.
9. Ve a la sección `Discover` y visualiza los datos ingestados.

Ayuda en la sección oficial de [configuración de logstash](https://www.elastic.co/guide/en/logstash/current/configuration.html)

El laboratorio se completa configurando correctamente el pipeline y para poder trabajar con las herramientas visuales que nos brinda Kibana, se ha de crear un `index pattern`.
