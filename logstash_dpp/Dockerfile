FROM docker.elastic.co/logstash/logstash:7.10.2
WORKDIR /data/elk
COPY pipelines.yml /usr/share/logstash/pipelines.yml
COPY logstash.yml /usr/share/logstash/logstash.yml
COPY pipeline/*.conf /data/elk/pipeline/
COPY mysql-connector-java-8.0.13.jar /data/elk/
#COPY mysql-connector-java-8.0.13.jar /usr/share/logstash/logstash-core/lib/jars/
#USER root
#RUN chmod 777 /usr/share/logstash/logstash-core/lib/jars/mysql-connector-java-8.0.13.jar