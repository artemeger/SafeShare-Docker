FROM    adoptopenjdk/openjdk12:jdk-12.0.2_10-slim

ARG     APP_PORT
ENV     APP_PORT ${APP_PORT}

RUN     apt-get update -yq &&\
        apt-get upgrade -yq &&\
        apt-get install -yq \
        unzip\
        git\
        maven\
        wget

RUN     git clone https://github.com/yuomii/SafeShare.git

CMD     mvn -f SafeShare -pl application-safeshare -am spring-boot:run