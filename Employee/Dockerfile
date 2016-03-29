FROM java:8
VOLUME /tmp
ADD build/libs/Employee-0.0.1-SNAPSHOT.jar app.jar
EXPOSE 8091
RUN bash -c 'touch /app.jar'
ENTRYPOINT ["java","-Dspring.data.mongodb.uri=mongodb://mongodb/micros","-Dserver.port=8091","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]