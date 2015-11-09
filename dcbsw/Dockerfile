FROM centos:7

ADD cross-2.95.3.tar.bz2 /usr/local/arm
ADD arm-linux-3.3.1-toolchain.tgz /usr/local/arm
ENV PATH /usr/local/arm/3.3.1/bin:$PATH

RUN yum update -y && yum install -y \
autoconf \
automake \
git \
glibc.i686 \
libtool \
make \
subversion \
xclock

RUN groupadd -r trd && useradd -r -m -g trd trd
USER trd
WORKDIR /home/trd

CMD ["/bin/bash", "-l"]
