FROM java:7

RUN apt-get update && apt-get install -y git wget libgradle-core-java

RUN git clone https://github.com/Netflix/recipes-rss.git

WORKDIR ./recipes-rss/
RUN ./gradlew clean build -x javadoc

#CMD java -Da.c.c=http://eureka_myhostname:port/.... -jar ./*.jar

ENV APP_ENV=dev 
CMD java -jar rss-edge/build/libs/rss-edge-*SNAPSHOT.jar
