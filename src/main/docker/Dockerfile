FROM java:8-alpine
RUN apk add --no-cache bash && \
    apk add --no-cache curl
EXPOSE 8761
ENTRYPOINT ["java","-Xmx512m","-Djava.security.egd=file:/dev/./urandom","-cp","$JAVA_HOME/lib/*:/lean/java/lib/*:/discovery-service.jar","org.thoughtworks.lean.discovery.Application"]
COPY lib /lean/java/lib
ADD discovery-service-1.0-SNAPSHOT.jar /discovery-service.jar