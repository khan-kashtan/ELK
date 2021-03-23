Misroservices
#### An application with ELK logging system. Default ports:
* UI     port 9292
* Kibana port 5601
* Zipkin port 9411

1. Build fluentd container:
``` bash
export username=<username>
cd src/logging/fluentd && docker build -t $username/fluentd . && cd ../../..
```
2. Deploy application:
``` bash
cd src/docker && docker-compose up -d && cd ../..
```
3. Deploy EFK:
``` bash
cd src/docker && docker-compose -d docker-compose-logging.yml up -d && cd ../..
```