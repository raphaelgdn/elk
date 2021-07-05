FROM elk/java_image:latest
LABEL description="Raphael Neves"

ENV DEBIAN_FRONTEND noninteractive

RUN \
 wget https://artifacts.elastic.co/downloads/kibana/kibana-7.13.2-linux-x86_64.tar.gz && \
 tar xvzf kibana-7.13.2-linux-x86_64.tar.gz && \
 rm -f kibana-7.13.2-linux-x86_64.tar.gz && \
 chown -R esuser:esuser kibana-7.13.2-linux-x86_64

ADD kibana.yml kibana-7.13.2-linux-x86_64/config/kibana.yml

ENTRYPOINT kibana-7.13.2-linux-x86_64/bin/kibana --allow-root