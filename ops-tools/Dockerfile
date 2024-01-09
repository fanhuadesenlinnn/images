FROM ubuntu:22.04

ENV test=test


RUN apt-get update   \
    && apt-get install -y curl wget \
    # bendsql
    && curl -L -o /etc/apt/sources.list.d/datafuselabs.sources https://repo.databend.rs/deb/datafuselabs.sources \
    && apt-get update  \
    && apt-get install -y bendsql mysql-client \
                          git fping  \
    $$ wget https://dl.min.io/client/mc/release/linux-amd64/mc  \
    && chmod +x mc     \
    && mv mv /bin/   \
    && rm -rf /var/lib/apt/lists/* 


WORKDIR /

CMD sleep "3600"
