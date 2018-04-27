# Use an official Tomcat runtime as a parent image
FROM tomcat:7-jre8

RUN apt-get update && apt-get install -y wget openjdk-8-jdk git

RUN wget http://search.maven.org/remotecontent?filepath=com/netflix/eureka/eureka-server/1.8.7/eureka-server-1.8.7.war

ADD server.xml /usr/local/tomcat/conf/

RUN cp ./*.war /usr/local/tomcat/webapps/eureka.war

EXPOSE 8080