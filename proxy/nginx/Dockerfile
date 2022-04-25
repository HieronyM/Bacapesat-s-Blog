FROM nginx:latest

MAINTAINER Hierony Manurung (hieronymilanisti09@gmail.com)

RUN apt-get update \
        && apt-get install wget -y \
        && apt-get install openssl --no-install-recommends --no-install-suggests -y \
        && rm -fr /var/lib/apt/lists/*

#Install Prerequisites
RUN apt-get update \
       && apt-get install -qqy curl python apt-transport-https apt-utils gnupg1 procps

#Install amplify
RUN wget https://github.com/nginxinc/nginx-amplify-agent/raw/master/packages/install.sh && \
    chmod +x install.sh && \
    API_KEY='e89c6a16be54a83cd48d45a17a37bd9a' sh ./install.sh -y 
