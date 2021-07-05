FROM elk/java_image:latest
LABEL description="Raphael Neves"

ENV DEBIAN_FRONTEND noninteractive

RUN \
 wget https://artifacts.elastic.co/downloads/beats/filebeat/filebeat-7.13.2-linux-x86_64.tar.gz && \
 tar zxvf filebeat-7.13.2-linux-x86_64.tar.gz && \
 rm -f filebeat-7.13.2-linux-x86_64.tar.gz

ADD filebeat.yml filebeat-7.13.2-linux-x86_64/filebeat.yml