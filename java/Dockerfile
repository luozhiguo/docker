FROM registry.cn-beijing.aliyuncs.com/zxit/centos:7.6
MAINTAINER lzg <lzg3251@gmail.com>

ENV JAVA_HOME /usr/java/jdk1.8.0_141
ENV PATH=$JAVA_HOME/bin:$PATH

RUN curl -L -H "Cookie: oraclelicense=accept-securebackup-cookie" -o /tmp/jdk.tar.gz "http://download.oracle.com/otn-pub/java/jdk/8u141-b15/336fa29ff2bb4ef291e347e091f7f4a7/jdk-8u141-linux-x64.tar.gz" \
    && mkdir -p /usr/java && tar -xzf /tmp/jdk.tar.gz -C /usr/java && rm /tmp/jdk.tar.gz \
    && cd /usr/bin && ln -s /usr/java/jdk1.8.0_141/bin/java . \
    && echo  "export JAVA_HOME=/usr/java/jdk1.8.0_141" >/etc/profile.d/java.sh \
    && echo  "export PATH=\$JAVA_HOME/bin:\$PATH" >>/etc/profile.d/java.sh \
    && chmod 644 /etc/profile.d/java.sh

