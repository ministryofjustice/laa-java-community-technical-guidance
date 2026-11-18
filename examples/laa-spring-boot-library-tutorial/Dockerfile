# Specify java runtime base image
FROM ghcr.io/ministryofjustice/laa-base-container-images/java:25-corretto-alpine

USER root

# Set up working directory in the container
RUN mkdir -p /opt/laa-spring-boot-library-tutorial/
WORKDIR /opt/laa-spring-boot-library-tutorial/

# Copy the JAR file into the container
COPY laa-spring-boot-library-tutorial-service/build/libs/laa-spring-boot-library-tutorial-service-1.0.0.jar app.jar

# Set the default user
USER 1001

# Expose the server.port and management.server.port for the application
EXPOSE 8081 8181

# Run the JAR file
CMD java -jar app.jar