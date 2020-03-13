FROM rwngallego/asdf:centos7.7

SHELL ["/bin/bash", "-c", "-l"]

ENV ERLANG_VERSION 22.2.8
ENV ELIXIR_VERSION 1.10.2

RUN asdf plugin-add erlang https://github.com/asdf-vm/asdf-erlang.git
RUN asdf plugin-add elixir https://github.com/asdf-vm/asdf-elixir.git
RUN asdf install erlang ${ERLANG_VERSION}
RUN asdf install elixir ${ELIXIR_VERSION}
RUN asdf global erlang ${ERLANG_VERSION}
RUN asdf global elixir ${ELIXIR_VERSION}

RUN mix local.hex --force
RUN mix local.rebar --force
