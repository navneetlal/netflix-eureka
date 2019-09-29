FROM openjdk:8-jre-alpine
RUN apk --no-cache add curl
HEALTHCHECK --start-period=30s --interval=5s CMD curl -f http://localhost:8761/health || exit 1
CMD java -jar eureka-0.0.1-SNAPSHOT.jar --server.port=8761
EXPOSE 8761
COPY target/eureka-0.0.1-SNAPSHOT.jar .