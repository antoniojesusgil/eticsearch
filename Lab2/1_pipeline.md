### Some words here
Logstash necesita de ficheros de configuración para realizar la ingesta en elasticsearch.

##### To-Do

```code

# Sección de entrada

input {
	stdin {
		type => "stdin-type"
		codec => plain { charset => "UTF-8" }
	}
	file {
		path => ["./data/*.csv"]
		start_position => "beginning"
		sincedb_path => "/dev/null"
	}
}

# Sección de filtrado

filter {
	csv {
		skip_header => true 
		separator => ","
		columns => ["Fecha","Aplicacion","Pais","Dispositivo","Instalaciones","Desinstalaciones","Impresiones"]
	}  
}

# Sección de salida

output {
	elasticsearch {
		action=>"index"
		hosts => "http://127.0.0.1:9200"
		index => "apps"
		manage_template => false
	}
	stdout { codec => rubydebug }
}
````
