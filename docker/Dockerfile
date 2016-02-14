FROM ubuntu:14.04.3
RUN apt-get update
RUN apt-get upgrade -y

# ruby related packages for td-agent
RUN apt-get -y install curl libcurl4-openssl-dev ruby ruby-dev make

RUN apt-get -y install vim

# install fluentd td-agent
RUN curl -L http://toolbelt.treasuredata.com/sh/install-ubuntu-trusty-td-agent2.sh | sh

CMD [ "/bin/bash" ]
