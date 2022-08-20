# Filebeat

Filebeat es un cargador ligero para reenviar y centralizar datos de registro. Instalado como un agente en sus servidores, Filebeat monitorea los archivos de registro o las ubicaciones que especifique, recopila eventos de registro y los reenvía a Elasticsearch o Logstash para su indexación.

## Uso

Para incluir Filebeat en la pila, ejecute Docker Compose desde la raíz del repositorio haciendo referencia al archivo `docker-compose.yml`:

```console
$ docker-compose up
```

## Configuración de Filebeat

La configuración de Filebeat se almacena en [`config/filebeat.yml`](./config/filebeat.yml). Puede modificar este archivo con la ayuda de la [referencia de configuración][filebeat-config].

Cualquier cambio en la configuración de Filebeat requiere un reinicio del contenedor de Filebeat:

```console
$ docker-compose restart filebeat
```

Consulte la siguiente página de documentación para obtener más detalles sobre cómo configurar Filebeat dentro de un contenedor Docker: [Ejecute Filebeat en Docker][filebeat-docker].

## Ver también

[Filebeat documentation][filebeat-doc]

[filebeat-config]: https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-reference-yml.html
[filebeat-docker]: https://www.elastic.co/guide/en/beats/filebeat/current/running-on-docker.html
[filebeat-doc]: https://www.elastic.co/guide/en/beats/filebeat/current/index.html
