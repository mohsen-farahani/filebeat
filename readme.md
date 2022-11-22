# Filebeat

## Ship logs from Docker to Elasticsearch

We use the official beats docker image.

### Settings
Before starting Filebeat, you should look at the configuration options in the configuration file.

The configuration file has been located at ` config/filebeat.yml`.

### ENV
To use the repository, You need to set these environment values.

Variable | Default | Description
-------- | ------- | -----------
FILEBEAT_VERSION | 8.5.1 | Filebeat version from the official docker image
ELASTIC_HOST | elasticsearch | Elasticsearch host
ELASTIC_PORT | 9200 | Elasticsearch port
ELASTIC_USERNAME | elastic | Elasticsearch username for HTTP auth
ELASTIC_PASSWORD | changeme | Elasticsearch password

### Format
The format which You have to follow in your applications to use Filebeat:

```
app-log - %{environment} - %{level} - %{event.time} - %{event.message} - %{event.context} - %{event.extra}
```
