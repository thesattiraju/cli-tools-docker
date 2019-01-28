FROM alpine:latest

LABEL version="1.0.0"

LABEL maintainer="Deepak Sattiraju"

RUN apk add --update -t deps curl tar gzip openssl
RUN apk update \
  && rm -rf /var/cache/apk/* \
  && curl https://github.com/kubernetes-sigs/kustomize/releases/download/v1.0.11/kustomize_1.0.11_linux_amd64 -Lo kustomize\
  && chmod +x ./kustomize \
  && mv ./kustomize /usr/local/bin/kustomize

ENTRYPOINT ["/usr/local/bin/kustomize"]