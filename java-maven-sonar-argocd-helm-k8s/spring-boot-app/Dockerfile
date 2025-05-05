# Use Eclipse Temurin JDK 17 base image
FROM eclipse-temurin:17-jdk-alpine

# Install Docker CLI and Maven
RUN apk update && apk add --no-cache docker maven

# Set working directory
WORKDIR /opt/app

# ARG for Maven artifact
ARG artifact=target/spring-boot-web.jar

# Copy JAR file
COPY ${artifact} app.jar

# Default command
ENTRYPOINT ["java", "-jar", "app.jar"]
