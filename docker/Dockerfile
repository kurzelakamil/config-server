# Start with a base image containing Java runtime
FROM openjdk:11-jdk-slim

# Add Maintainer Info
LABEL maintainer="kurzela.kamil@gmail.com"

# Make port 8888 available to the world outside this container
EXPOSE 8888

# The application's jar file
ARG JAR_FILE=config-server.jar

# Add the application's jar to the container
ADD ${JAR_FILE} config-server.jar

# Run the jar file
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/config-server.jar"]