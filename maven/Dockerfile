FROM registry.cn-beijing.aliyuncs.com/zxit/jdk:1.8
MAINTAINER lzg <lzg3251@gmail.com>

ARG MAVEN_VERSION=3.6.3

ENV MAVEN_HOME /usr/share/maven

RUN curl -fsSL -o /tmp/apache-maven.tar.gz https://apache.osuosl.org/maven/maven-3/${MAVEN_VERSION}/binaries/apache-maven-${MAVEN_VERSION}-bin.tar.gz \
  && mkdir -p /usr/share/maven && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1 \
  && rm -f /tmp/apache-maven.tar.gz \
  && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn

VOLUME "$MAVEN_HOME/.m2"

