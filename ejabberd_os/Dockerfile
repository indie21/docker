FROM ubuntu
RUN apt-get update

RUN DEBIAN_FRONTEND=noninteractive apt-get install  -y mysql-server mysql-client
RUN apt-get install -y telnet
RUN apt-get install -y htop
RUN apt-get install -y autoconf
RUN apt-get install -y automake
RUN apt-get install -y make
RUN apt-get install -y build-essential
RUN apt-get install -y openssl
RUN apt-get install -y libncurses5-dev
RUN apt-get install -y libssl-dev


RUN wget http://erlang.org/download/otp_src_18.3.tar.gz
RUN tar -xzvf otp_src_18.3.tar.gz
RUN cd otp_src_18.3; ./configure;make ;make install; cd -

RUN apt-get install -y git

COPY .ssh /root/.ssh

RUN apt-get install -y libyaml-dev
RUN apt-get install -y libexpat1-dev
RUN apt-get install -y elixir


COPY ./run.sh /srv/source/
WORKDIR /srv/source/
ENTRYPOINT ["bash", "run.sh"]

