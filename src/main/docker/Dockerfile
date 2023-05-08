# syntax=docker/dockerfile:1

#FROM eclipse-temurin:17-jdk-jammy
#
#WORKDIR /app
#
#COPY ../../../.mvn .mvn
#COPY ../../../mvnw pom.xml ./
#RUN ./mvnw dependency:resolve
#
#COPY ../.. ./src
#
#CMD ["./mvnw", "spring-boot:run"]

FROM eclipse-temurin:17-jdk-jammy

MAINTAINER fuwenkai 'fwkilyaw@qq.com'
VOLUME /tmp
ADD spring-petclinic-3.0.0-SNAPSHOT.jar /
#RUN bash -c 'touch /spring-petclinic-3.0.0-SNAPSHOT.jar'
#EXPOSE 8081

#ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom spring.profiles.active=mysql","-jar","spring-petclinic-3.0.0-SNAPSHOT.jar"]
ENTRYPOINT ["sh","-c","java -jar spring-petclinic-3.0.0-SNAPSHOT.jar -Djava.security.egd=file:/dev/./urandom --spring.profiles.active=$PROFILES "]
