# docker-session

Add a config file with the below properties in your local folder :

server:
  port: 8081
spring:
  application:
    name: DEMO-SERVICE
eureka:
  instance:
    prefer-ip-address: true

for eg: C:\Users\skarv\IdeaProjects\config

Then while running the container:

 docker run --name demo-service -d -p 8080:8081 -v C:\Users\skarv\IdeaProjects\config:/etc/config -e "eureka.client.service-url.defaultZone=http://172.17.0.2:8761/eureka" <image_id>
