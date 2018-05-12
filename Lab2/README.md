# Logstash from scratch

Logstash es la herramienta para ingestar datos en elasticsearch, brinda un amplio abanico de filtros para modificar y transformar los datos crudos a datos entendibles por el área de negocio y posterior análisis.

#### Enunciado:

Una de las áreas de negocio de nuestra compañia está centrada en el desarrollo de apps moviles, tras el lanzamiento de la primera, la dirección desea conocer el impacto de la misma a nivel global.

Las estadísticas que nos brindan los dos principales markets tan solo contemplan su área. La dirección desea que tengamos unos indicadores globales y nos piden que añadamos un nuevo índice en elastic para posteriormente construir un dashboard.

##### To-Do
Para completar el laboratorio se ha de configurar correctamente el fichero de configuración que se le pasará a logstash, se pide:

1. Descarga los datos estadisticos correspondiente a Google y Apple
2. Descarga y utiliza la plantilla `pipeline.conf` para construir el script. 
3. Modifica el script para que apunte a los archivos csv
4.- Convertir los campos numericos en integer:
>Utiliza mutate para transformar "Instalaciones", "Desinstalaciones" e "Impresiones"

2.- Indica que la columna "Fecha" es de tipo date.
>Ten en cuenta los distintos formatos que vienen en los archivos csv

3. Crea un índice llamado `markets`

Para completar el laboratorio se ha de configurar correctamente el fichero de configuración que se le pasará a logstash 

### Comprobar que se ha creado el índice y mostrar los datos en la consola 

Para poder trabajar con las herramientas visuales que nos brinda Kibana, hemos de crear un `index pattern`
