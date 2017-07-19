FROM centos
MAINTAINER ahaii

RUN groupadd -r mongo && useradd -r -g mongo mongo
RUN yum install -y gcc gcc-c++ net-tools make
RUN mkdir /data && chown -R mongo:mongo /data
RUN mkdir /data/mongo_data
VOLUME ["/data"]
ADD mongodb-3.2.0.tgz /data/
ENV PATH=$PATH:/data/mongodb-3.2.0/bin
WORKDIR /data/mongodb-3.2.0/bin
COPY mongo.conf .
EXPOSE 27017
CMD ["mongod","-f", "mongo.conf"]
