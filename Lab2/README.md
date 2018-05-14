# Logstash

Logstash es la herramienta máter de elastic, brinda un amplio abanico de filtros para modificar, transformar e ingestar cantidades masivas de datos crudos a datos entendibles por las áreas de negocio y su posterior análisis.

### Objetivos

Toma de contacto con logstash, aprender a elaborar scripts para añadir datos en elasticsearch y poder visualizar los mismos en Kibana.

Este laboratorio consta de dos partes, la primera, enunciada a continuación indica paso por paso que hemos de hacer para construir el script pipeline y crear un índice. 

En la segunda aprenderemos a añadir nuevos datos necesarios analizando los originales para disponer de información más relevante.

### To-Do

1. Descarga los datos estadisticos del directorio `data`.
2. Descarga y utiliza la plantilla `pipeline.conf` para construir el script. 
3. Modifica el script para que apunte a los archivos csv.
4. Convertir los campos numericos en integer:
>Utiliza mutate para transformar `Instalaciones | Desinstalaciones | Impresiones` 

5. Indica que la columna `Fecha` es de tipo date.
>Ten en cuenta los formatos fecha que vienen en los archivos csv.

6. Ejecuta logstash contra elasticsearch y crea un índice llamado `markets`.
>Para indicar a logstash que utilize el script hay que pasar el flag `-f`
>Ejecuta `bin/logstash -f pipeline.conf`

7. Comprobar que se ha creado el índice, visualiza la consola.
8. Crear el index pattern en kibana.
9. Ve a la sección `Discover` y visualiza los datos ingestados.

Ayuda en la sección oficial de [configuración de logstash](https://www.elastic.co/guide/en/logstash/current/configuration.html)

El laboratorio se completa configurando correctamente el pipeline y para poder trabajar con las herramientas visuales que nos brinda Kibana, se ha de crear un `index pattern`.

Una vez resuelta esta primera fase, ve a la segunda pinchando [aquí](./Lab2_1/README.md)
