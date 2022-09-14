FROM openjdk:8
ADD target/demo-service.jar demo-service.jar
ENTRYPOINT ["java","-jar","-Dspring.config.additional-location=file:/etc/config/application.yml","/demo-service.jar"]


#docker run --name demo-service -d -p 8080:8082 -v C:\Users\skarv\IdeaProjects\config:/etc/config 9feeec0b6478