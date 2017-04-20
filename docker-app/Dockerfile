FROM docker-release-local2.demo.jfrogchina.com/docker-framework:latest

MAINTAINER Liu yongqiang@jfrog.com

ADD war/*.war /home/exec/apache-tomcat-8.5.5/webapps/swampup.war

CMD /bin/bash -c cd /home/exec; /home/exec/apache-tomcat-8.5.5/bin/catalina.sh run
