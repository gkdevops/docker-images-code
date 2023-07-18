FROM eclipse-temurin:11

WORKDIR /home/sales/app

COPY spring-boot-docker.jar app.jar

ENV server.port=9090

CMD ["java", "-jar", "app.jar"]
