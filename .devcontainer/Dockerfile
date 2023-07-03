FROM docker.io/golang:1.20.5-bullseye AS golang

FROM kraftkit.sh/base:latest

COPY --from=golang /usr/local/go /usr/local/go


RUN apt-get update && \
    export DEBIAN_FRONTEND=noninteractive && \
    apt-get -y install --no-install-recommends curl g++

ENV PATH="$PATH:/usr/local/go/bin"

