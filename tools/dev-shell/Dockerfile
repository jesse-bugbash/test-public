# syntax=docker/dockerfile:1.7
FROM ubuntu:24.04

RUN --mount=type=cache,target=/var/cache/apt,sharing=locked \
    --mount=type=cache,target=/var/lib/apt,sharing=locked \
    apt-get update && apt-get install -y --no-install-recommends \
      git curl zsh vim build-essential ca-certificates

COPY <<EOT /etc/motd
Welcome to the dev shell.
EOT

WORKDIR /work
CMD ["zsh"]
