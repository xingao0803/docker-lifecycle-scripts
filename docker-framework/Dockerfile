FROM ubuntu:latest

MAINTAINER yongqiang liuyq@jfrog.com

RUN /bin/bash -c cd ~; cd /home ; mkdir -p exec
ADD jdk/jdk-8-linux-x64.tar.gz /home/exec
#RUN /bin/bash -c cd /home/exec; mv /home/exec/jdk1* /home/exec/jdk8
ENV JAVA_HOME=/home/exec/jdk1.8.0_91
RUN sed "/securerandom.source=/{s/file:\/dev\/random/file:\/dev\/urandom/}" /home/exec/jdk1.8.0_91/jre/lib/security/java.security -i

ADD tomcat/apache-tomcat-8.tar.gz /home/exec
#RUN /bin/bash -c cd /home/exec; mv /home/exec/apache-tomcat-8.* /home/exec/tomcat
ADD tomcat/server.xml /home/exec/apache-tomcat-8.5.5/conf
ENV CATALINA_HOME=/home/exec/apache-tomcat-8.5.5

CMD /bin/bash -c cd /home/exec; /home/exec/apache-tomcat-8.5.5/bin/catalina.sh run
