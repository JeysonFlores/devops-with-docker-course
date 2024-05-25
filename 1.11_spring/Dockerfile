# Use Java 8 (as required by the project) and Alpine for lightweight image size
FROM amazoncorretto:8-alpine3.16

# Expose the port the app will connect to
EXPOSE 8080

# Create a workdir
WORKDIR /app

# Copy the files
COPY . .

# Install the dependencies
RUN ./mvnw package

# Command to run the project
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]