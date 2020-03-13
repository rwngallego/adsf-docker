FROM centos:7.7.1908

SHELL ["/bin/bash", "-c", "-l"]

RUN yum update -y

RUN localedef -c -f UTF-8 -i en_US en_US.UTF-8
ENV LC_ALL=en_US.UTF-8

RUN yum groupinstall -y 'Development Tools' 'C Development Tools and Libraries'
RUN yum install -y autoconf ncurses-devel openssl-devel
RUN git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.7.7
RUN echo -e '\n. $HOME/.asdf/asdf.sh' >> ~/.bashrc
RUN echo -e '\n. $HOME/.asdf/completions/asdf.bash' >> ~/.bashrc

RUN asdf update