FROM alpine as builder

RUN wget https://github.com/sigoden/dufs/releases/download/v0.39.0/dufs-v0.39.0-x86_64-unknown-linux-musl.tar.gz && \
    tar -xf dufs-v0.39.0-x86_64-unknown-linux-musl.tar.gz && \
    mv dufs /bin/

FROM scratch
COPY --from=builder /bin/dufs /bin/dufs
STOPSIGNAL SIGINT
ENTRYPOINT ["/bin/dufs"]