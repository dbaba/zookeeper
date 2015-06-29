FROM ubuntu:14.04

RUN apt-get update && apt-get install -y curl openjdk-7-jre-headless

RUN curl -fL http://mirror.catn.com/pub/apache/zookeeper/stable/zookeeper-3.4.6.tar.gz | tar xzf - -C /opt && mv /opt/zookeeper-3.4.6 /opt/zookeeper

VOLUME /tmp/zookeeper

COPY entrypoint.sh /

ENTRYPOINT ["/entrypoint.sh"]

CMD ["/opt/zookeeper/bin/zkServer.sh", "start-foreground"]