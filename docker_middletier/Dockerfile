FROM java:7

RUN apt-get update && apt-get install -y git wget libgradle-core-java

RUN git clone https://github.com/Netflix/recipes-rss.git

WORKDIR ./recipes-rss/
RUN ./gradlew clean build -x javadoc

ENV APP_ENV=dev
CMD java -jar rss-middletier/build/libs/rss-middletier-*SNAPSHOT.jar

EXPOSE 9191 9192


