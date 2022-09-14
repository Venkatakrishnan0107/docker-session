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
 
 docker run --name gateway -d -p 8083:8084 -e "eureka.client.service-url.defaultZone=http://172.17.0.2:8761/eureka" <image_id>
 
 docker run --name eureka -d -p 8761:8761 <image_id>
 
 
 ![image](https://user-images.githubusercontent.com/73943222/190118564-ae1e2c0b-7bd7-462c-873f-5c9488ebb210.png)

![image](https://user-images.githubusercontent.com/73943222/190118630-07c2437a-8782-42d3-be14-ae549270f856.png)

