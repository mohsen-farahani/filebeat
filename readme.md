# Filebeat

## Ship logs from Docker to Elasticsearch
We use official beats docker image.
<br></br>
### Settings
Before starting Filebeat, you should look at the configuration options in the configuration file.
please check config in:  ``` config/filebeat.yml```

<br></br>
#### please set env
Variable | Default | Description
-------- | ------- | -----------
FILEBEAT_VERSION | 8.5.1 | Filebeat version from official docker image
ELASTIC_HOST | elasticsearch | Elasticsearch host
ELASTIC_PORT | 9200 | Elasticsearch port
ELASTIC_USERNAME | elastic | Elasticsearch username for HTTP auth
ELASTIC_PASSWORD | changeme | Elasticsearch password

<br></br>
#### please use this format in application
``` app-log - %{environment} - %{level} - %{event.time} - %{event.message} - %{event.context} - %{event.extra} ```