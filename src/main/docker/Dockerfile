FROM registry.aliyuncs.com/leansw/java-base
EXPOSE 8761
VOLUME /tmp
ENTRYPOINT ["java","-Xmx512m","-Djava.security.egd=file:/dev/./urandom","-cp","$JAVA_HOME/lib/*:/lean/java/lib/*:/discovery-service.jar","org.thoughtworks.lean.discovery.Application"]
COPY lib /lean/java/lib
ADD discovery-service-*-SNAPSHOT.jar /discovery-service.jar
RUN touch /discovery-service.jar && \
    touch /lean/java/lib/*.jar