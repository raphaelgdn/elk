FROM ubuntu:20.04
LABEL description="Raphael Neves"

RUN apt update && apt upgrade -y && apt-get install openjdk-11-jre wget apt-transport-https curl gnupg2 -y

RUN useradd -d /home/esuser -m esuser && mkdir -p /home/esuser/data && \
chown -R esuser:esuser /home/esuser && chmod -R 775 /home/esuser/data

WORKDIR /home/esuser

ENV ES_JAVA_HOME /usr/lib/jvm/java-11-openjdk-amd64