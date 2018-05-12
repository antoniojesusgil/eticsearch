# Logstash from scratch

Logstash es la herramienta máter de elastic, brinda un amplio abanico de filtros para modificar, transformar e ingestar cantidades masivas de datos crudos a datos entendibles por las áreas de negocio y su posterior análisis.

#### Enunciado:

Una de las áreas de negocio de nuestra compañia está centrada en el desarrollo de apps moviles, tras el lanzamiento una de ellas, la dirección desea conocer el impacto de la misma a nivel global.

Las estadísticas que nos brindan los principales markets tan solo contemplan su área. La dirección desea que tengamos unos indicadores globales y nos piden que añadamos un nuevo índice en elastic para posteriormente construir un dashboard.

##### To-Do

1. Descarga los datos estadisticos correspondiente a Google y Apple.
2. Descarga y utiliza la plantilla `pipeline.conf` para construir el script. 
3. Modifica el script para que apunte a los archivos csv.
4. Convertir los campos numericos en integer:
>Utiliza mutate para transformar `Instalaciones | Desinstalaciones | Impresiones` 

5. Indica que la columna `Fecha` es de tipo date.
>Ten en cuenta los formatos fecha que vienen en los archivos csv.

6. Crea un índice llamado `markets`.
7. Comprobar que se ha creado el índice, visualiza la consola.

Ayuda en la sección oficial de [configuración de logstash](https://www.elastic.co/guide/en/logstash/current/configuration.html)

El laboratorio se completa configurando correctamente el pipeline y para poder trabajar con las herramientas visuales que nos brinda Kibana, se ha de crear un `index pattern`.
