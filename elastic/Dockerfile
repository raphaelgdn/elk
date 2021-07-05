FROM elk/java_image:latest
LABEL description="Raphael Neves"

ENV DEBIAN_FRONTEND noninteractive

RUN \
 wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-7.13.2-linux-x86_64.tar.gz && \
 tar xvzf elasticsearch-7.13.2-linux-x86_64.tar.gz && \
 rm -f elasticsearch-7.13.2-linux-x86_64.tar.gz && \
 chown -R esuser:esuser elasticsearch-7.13.2

# elasticsearch.yml and Dockerfile are on same location
 ADD elasticsearch.yml /home/esuser/elasticsearch-7.13.2/config/elasticsearch.yml
 ENTRYPOINT elasticsearch-7.13.2/bin/elasticsearch