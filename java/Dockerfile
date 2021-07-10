# This is a Dockerfile for Java

FROM tomcat:8.5.69-jdk8-openjdk-slim-buster

LABEL maintainer="devops@example.com"

COPY petclinic.war /usr/local/tomcat/webapps/

CMD ["catalina.sh", "run"]
