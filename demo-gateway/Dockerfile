FROM openjdk:8
EXPOSE 8083
ADD target/gateway.jar gateway.jar
ENTRYPOINT ["java","-jar","/gateway.jar"]