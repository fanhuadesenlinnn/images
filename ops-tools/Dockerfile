FROM ubuntu:latest

ENV test=test

WORKDIR /tem

RUN apt-get update   \
    && apt-get install -y curl wget \
    # bendsql
    && curl -L -o /etc/apt/sources.list.d/datafuselabs.sources https://repo.databend.rs/deb/datafuselabs.sources \
    && apt-get update  \
    && apt-get install -y bendsql mysql-client  \
                          git fping iputils-ping vim \
    && wget https://dl.min.io/client/mc/release/linux-amd64/mc  \
    && chmod +x mc     \
    && mv mc /bin/   \
    && rm -rf /var/lib/apt/lists/* 


WORKDIR /

CMD sleep "3600"
