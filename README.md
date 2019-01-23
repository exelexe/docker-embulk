# docker-embulk
An AlpineLinux Embulk docker container.

## Tags

- [`0.9.12-alpine3.8`, `latest`](https://github.com/exelexe/docker-embulk/tree/master/0.9.12/alpine3.8/Dockerfile)
- [`0.9.9-alpine3.8`](https://github.com/exelexe/docker-embulk/tree/master/0.9.9/alpine3.8/Dockerfile)

## How to use?

For example

```dockerfile
FROM exelexe/embulk:latest

RUN adduser -D embulk
USER embulk

RUN embulk gem install \
        embulk-input-mysql \
        embulk-output-bigquery

WORKDIR /usr/src
COPY --chown=embulk:embulk . .
```
