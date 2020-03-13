FROM rwngallego/asdf:centos7.7-elixir

SHELL ["/bin/bash", "-c", "-l"]

ENV NODE_VERSION 12.16.1

RUN asdf plugin-add nodejs https://github.com/asdf-vm/asdf-nodejs.git
RUN bash ~/.asdf/plugins/nodejs/bin/import-release-team-keyring

RUN asdf install nodejs ${NODE_VERSION}
RUN asdf global nodejs ${NODE_VERSION}
