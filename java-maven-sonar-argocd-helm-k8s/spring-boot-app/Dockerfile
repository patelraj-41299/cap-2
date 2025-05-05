# Use Eclipse Temurin JDK 17 base image (supports Java 17)
FROM eclipse-temurin:17-jdk-alpine

# Install Docker CLI
RUN apk update && apk add --no-cache docker

# ARG for Maven artifact
ARG artifact=target/spring-boot-web.jar

# Create app directory
WORKDIR /opt/app

# Copy JAR file into image
COPY ${artifact} app.jar

# Keep the container alive for Jenkins pipeline use
CMD ["tail", "-f", "/dev/null"]
