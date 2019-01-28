FROM alpine:latest

LABEL version="1.0.0"

LABEL maintainer="Deepak Sattiraju"

RUN apk add --update -t deps curl tar gzip openssl
RUN apk update \
  && rm -rf /var/cache/apk/* \
  && curl https://raw.githubusercontent.com/helm/helm/master/scripts/get | sh 

ENTRYPOINT ["/usr/local/bin/helm"]