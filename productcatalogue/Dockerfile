FROM openjdk:8-jre

# Add the JAR file and configuration file to the image
ADD target/productcatalogue-0.0.1-SNAPSHOT.jar app.jar
ADD product-catalogue.yml app-config.yml

# Expose the port the app runs on
EXPOSE 8024

# Define the command to run the JAR file
ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "-jar", "app.jar", "server", "app-config.yml"]
