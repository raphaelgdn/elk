FROM alpine:latest
LABEL description="Raphael Neves"

RUN apk add openjdk11

ENV USER=esuser
ENV UID=12345
ENV GID=23456

RUN addgroup -S "$USER" && \
    adduser \
    -D \
    -g "" \
    -h /home/"$USER" \
    --ingroup "$USER" \
    --uid "$UID" \
    "$USER" && \ 
    mkdir /home/"$USER"/data && \
chown -R esuser:esuser /home/esuser && chmod -R 775 /home/esuser/data

WORKDIR /home/esuser

ENV ES_JAVA_HOME /usr/lib/jvm/java-11-openjdk/