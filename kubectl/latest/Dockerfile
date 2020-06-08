FROM  alpine:3.7

RUN   apk add --no-cache curl ca-certificates git openssh

RUN   cd /tmp \
      && curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl \
      && chmod +x /tmp/kubectl \
      && mv /tmp/kubectl /usr/local/bin
