# fluentd-stack
Montagem de ambiente contendo todos os arquivos necessários para a utilização de uma instânciafuncional do fluentd (contendo EFK).

### Utilização

```$ docker-compose up```

```$ docker ps```

```
CONTAINER ID        IMAGE                 COMMAND                  CREATED             STATUS              PORTS                                                          NAMES
e4c6148c31a8        httpd                 "httpd-foreground"       x seconds ago       Up x seconds        0.0.0.0:80->80/tcp                                             fluentd_web_1
a5aa8acba9ce        efk-docker_fluentd    "tini -- /bin/entryp…"   x seconds ago       Up x seconds        5140/tcp, 0.0.0.0:24224->24224/tcp, 0.0.0.0:24224->24224/udp   fluentd_fluentd_1
1548b060b0f6        kibana:5.3.0          "/docker-entrypoint.…"   x seconds ago       Up x seconds        0.0.0.0:5601->5601/tcp                                         fluentd_kibana_1
32a69da151d8        elasticsearch:5.3.0   "/docker-entrypoint.…"   x seconds ago       Up x seconds        0.0.0.0:9200->9200/tcp, 9300/tcp                               fluentd_elasticsearch_1
```
