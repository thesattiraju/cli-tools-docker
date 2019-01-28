FROM alpine:latest

LABEL version="1.0.0"

LABEL maintainer="Deepak Sattiraju"

RUN apk add --update -t deps curl tar gzip openssl
RUN apk update \
  && rm -rf /var/cache/apk/* \
  && curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl \
  && chmod +x ./kubectl \
  && mv ./kubectl /usr/local/bin/

ENTRYPOINT ["/usr/local/bin/kubectl"]