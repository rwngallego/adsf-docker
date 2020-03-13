# Elixir docker image

This docker image is built on top of Centos 7 using `asdf`.

## Contains

Plugins for `asdf` installed:

- Erlang
- Elixir

Mix packages:

- hex
- rebar

## Build

```
docker build -f centos7.7/Dockerfile -t rwngallego/asdf:centos7.7 .
docker build -f centos7.7-elixir/Dockerfile -t rwngallego/asdf:centos7.7-elixir .
docker run -it centos7.7-elixir /bin/bash -l
```
