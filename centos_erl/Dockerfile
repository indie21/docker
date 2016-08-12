FROM centos
RUN yum -y update
RUN yum -y install wget
RUN yum -y install sudo
RUN yum install -y ncurses-devel
RUN yum install -y openssl
RUN yum install -y git
RUN yum install -y openssl-devel
RUN yum install -y libyaml-devel
RUN yum install -y expat-devel
RUN yum install -y gcc-c++
RUN wget http://erlang.org/download/otp_src_18.3.tar.gz
RUN tar -xzvf otp_src_18.3.tar.gz
RUN cd otp_src_18.3; ./configure  ;make ;make install; cd -
RUN yum -y install autoconf
RUN yum -y install automake
RUN yum -y install make
COPY .ssh /root/.ssh