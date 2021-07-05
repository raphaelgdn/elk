FROM elk/java_image:latest
LABEL description="Raphael Neves"

ENV DEBIAN_FRONTEND noninteractive

RUN \
 wget https://artifacts.elastic.co/downloads/logstash/logstash-7.13.2-linux-x86_64.tar.gz && \
 tar xvzf logstash-7.13.2-linux-x86_64.tar.gz && \
 rm -f logstash-7.13.2-linux-x86_64.tar.gz && \
 chown -R esuser:esuser logstash-7.13.2
 
# logstash.conf and Dockerfile are on same location
 ADD logstash.conf /home/esuser

CMD logstash-7.13.2/bin/logstash -f logstash.conf --verbose