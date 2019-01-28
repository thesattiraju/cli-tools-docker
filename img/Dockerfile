FROM alpine:latest

LABEL version="1.0.0"

LABEL maintainer="Deepak Sattiraju"

RUN apk add --update -t deps curl tar gzip openssl
RUN apk update \
  && rm -rf /var/cache/apk/* \
  && curl -fSL "https://github.com/genuinetools/img/releases/download/v0.5.6/img-linux-amd64" -o "/usr/local/bin/img" \
  && echo "f5d686465a7463c296e94634bd9597af58544ead924567c9128a4ee352591bf1  /usr/local/bin/img" | sha256sum -c - \
  && chmod a+x "/usr/local/bin/img"

ENTRYPOINT ["/usr/local/bin/img"]