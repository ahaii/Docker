FROM centos

MAINTAINER ahaii

RUN groupadd -r redis && useradd -r -g redis redis
RUN mkdir /data && chown redis:redis /data
VOLUME ["/data"]
ADD redis-3.2.8.tar.gz /data/
RUN yum install -y gcc gcc-c++ net-tools make
WORKDIR /data/redis-3.2.8/src/
RUN make && make install
Copy redis-slave.conf .
EXPOSE 6802
CMD ["redis-server","redis-slave.conf"] 
