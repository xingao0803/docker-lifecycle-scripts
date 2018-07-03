FROM docker-dev-local.art.train/docker-framework:latest

MAINTAINER Mark Galpin markg@jfrog.com

ADD war/*.war /home/exec/apache-tomcat-8.5.5/webapps/swampup.war

CMD /bin/bash -c cd /home/exec; /home/exec/apache-tomcat-8.5.5/bin/catalina.sh run
