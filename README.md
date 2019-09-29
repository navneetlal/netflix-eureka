# Supported tags and respective `Dockerfile` link
- [latest](https://github.com/navneetlal/netflix-eureka/tree/master/docker-images/11-jre), [11-jre](https://github.com/navneetlal/netflix-eureka/tree/master/docker-images/11-jre)
- [8-jre](https://github.com/navneetlal/netflix-eureka/blob/master/docker-images/8-jre)
- [8-jre-alpine](https://github.com/navneetlal/netflix-eureka/blob/master/docker-images/8-jre-alpine)
- [7-jre-alpine](https://github.com/navneetlal/netflix-eureka/blob/master/docker-images/7-jre-alpine)
- [7-jre-jessie](https://github.com/navneetlal/netflix-eureka/blob/master/docker-images/7-jre-jessie)

# What is Netflix Eureka?
As the Github repo for **Netflix's Eureka** registry says itself: “**Eureka** is a REST (Representational State Transfer) based service that is primarily used in the AWS cloud for locating services for the purpose of load balancing and failover of middle-tier servers.” — **Netflix**

 - [Link to Neflix Eureka github](https://github.com/Netflix/eureka)
 
## How to use this image?
Using of this image is very simple. You just have to pull this image and run by publishing the desired port.
```
docker run -p 8761:8761 navneetlalg/eureka:latest
```
OR you can also use `docker-compose.yml` to create a service. This is the prefered way since you will require to connect other services to **Eureka**
```
version: '3.1'
services:
  registry:
    image: navneetlalg/eureka:8-jre-alpine
    ports:
      - 8761:8761
```
This API is based on spring-boot, In case you want to make changes to any default configuration like ports, etc can be done by setting environment variables `SPRING_APPLICATION_JSON`.

You can find the more detailed description related to spring-boot configuration over [here.](https://docs.spring.io/spring-boot/docs/current/reference/html/boot-features-external-config.html)
