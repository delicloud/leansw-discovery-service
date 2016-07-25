FROM registry.aliyuncs.com/leansw/discovery-service-dep

VOLUME /tmp
ADD discovery-service-1.0-SNAPSHOT.jar discovery-service.jar
RUN bash -c 'touch /discovery-service.jar'

EXPOSE 8761

ENTRYPOINT ["java","-Xmx512m","-Djava.security.egd=file:/dev/./urandom","-cp","$JAVA_HOME/lib/*:/lean/java/lib/*:/discovery-service.jar","org.thoughtworks.lean.discovery.Application"]