FROM openjdk:8-jre-alpine
EXPOSE 8761
ADD *.jar /discovery-service.jar
CMD java -Xmx512m -Djava.security.egd=file:/dev/./urandom -jar /discovery-service.jar
