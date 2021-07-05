FROM elk/filebeat_image
LABEL description="Raphael Neves"
ENV DEBIAN_FRONTEND noninteractive

WORKDIR /home/esuser
RUN apt-get update
RUN apt-get install -y wget

RUN apt-get update
RUN apt-get -y install nginx pwgen python-setuptools curl git unzip vim rsyslog

RUN chown -R www-data:www-data /var/lib/nginx
RUN rm -v /etc/nginx/nginx.conf
ADD nginx.conf /etc/nginx/

WORKDIR /etc/nginx
CMD /home/esuser/filebeat-7.13.2-linux-x86_64/filebeat -c /home/esuser/filebeat-7.13.2-linux-x86_64/filebeat.yml >/dev/null 2>&1 & service nginx start