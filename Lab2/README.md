# Logstash from scratch

Logstash es la herramienta para ingestar datos en elasticsearch, brinda un amplio abanico de filtros para modificar y transformar los datos crudos a datos entendibles por el área de negocio y su posterior análisis.

### Para resolver el laboratorio, se propone:

### La ingesta de datos obtenidos de los markets Google y Apple en elasticsearch, creado un índice llamado `markets`
### Configurar el script que añada los datos de los archivos csv
### Para poder trabajar con las herramientas visuales que nos brinda Kibana, hemos de crear un `index pattern`

visualizaciones
### Comprobar que se ha creado el índice y mostrar los datos en la consola 

Para completar el laboratorio se ha de configurar correctamente el fichero de configuración que se le pasará a logstash 

##### To-Do
Utiliza la plantilla existente en el archivo pipeline para:
1.- Convertir los campos numericos en integer:
>Utiliza mutate para transformar "Instalaciones", "Desinstalaciones" e "Impresiones"

2.- Indica que la columna "Fecha" es de tipo date.
>Ten en cuenta los formatos
