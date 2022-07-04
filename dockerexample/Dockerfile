# syntax= docker/dockerfile:1
# which "offile java image"
FROM openjdk:oraclelinux8
#working directory
WORKDIR /app
# coppy from your Host to container
COPY .mvn/ .mvn
COPY mvnw pom.xml ./
#run this inside the image
RUN ./mvnw dependency:go-offline
COPY src ./src
#run inside container
CMD ["./mvnw","spring-boot:run"]


