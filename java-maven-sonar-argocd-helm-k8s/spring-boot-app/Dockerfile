FROM eclipse-temurin:17-jdk-alpine

# Install Docker CLI, Maven, and Git
RUN apk update && apk add --no-cache docker maven git

# Set working directory
WORKDIR /opt/app

# Optional: ARG for jar location if needed later
ARG artifact=target/spring-boot-web.jar
COPY ${artifact} app.jar

# Use CMD instead of ENTRYPOINT to avoid immediate execution during Jenkins pipeline
CMD ["java", "-jar", "app.jar"]
