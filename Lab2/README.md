# Logstash from scratch

Logstash es la herramienta para ingestar datos en elasticsearch, brinda un amplio abanico de filtros para modificar y transformar los datos crudos a datos entendibles por el área de negocio y posterior análisis.

### Enunciado:

Una de las áreas de negocio de nuestra compañia está centrada en el desarrollo de apps moviles, tras el lanzamiento de la primera, la dirección desea conocer el impacto de la misma a nivel global.

Las estadísticas que nos brindan los dos principales markets tan solo contemplan su área. La dirección desea que tengamos unos indicadores globales y nos piden que añadamos un nuevo índice en elastic para posteriormente construir un dashboard.

##### To-Do

1. Descarga los datos estadisticos correspondiente a Google y Apple
2. Utiliza la plantilla `pipeline.conf` 
so completas, aunque ajustadas as su Tenemos aplicaciones
### La ingesta de datos obtenidos de los markets Google y Apple en elasticsearch, creado un índice llamado `markets`
### Configurar el script que añada los datos de los archivos csv
### Para poder trabajar con las herramientas visuales que nos brinda Kibana, hemos de crear un `index pattern`

visualizaciones
### Comprobar que se ha creado el índice y mostrar los datos en la consola 

Para completar el laboratorio se ha de configurar correctamente el fichero de configuración que se le pasará a logstash 

Utiliza la plantilla existente en el archivo pipeline para:
1.- Convertir los campos numericos en integer:
>Utiliza mutate para transformar "Instalaciones", "Desinstalaciones" e "Impresiones"

2.- Indica que la columna "Fecha" es de tipo date.
>Ten en cuenta los formatos
