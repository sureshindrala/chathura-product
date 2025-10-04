# Instructions

# This is the official image as a base
FROM openjdk:18

# Create a directory called /opt/chathura  in which we store our artifacts or other read only data.
RUN mkdir -p /opt/chathura/

# Setting the working directory to /opt/chathura
WORKDIR /opt/chathura/

# Define a build time variable called JAR_SOURCE to specify the path format
ARG JAR_SOURCE

COPY ["${JAR_SOURCE}", "/opt/chathura/chathura-product.jar"]

# Grant permissions to the Workdir 
RUN chmod 777 /opt/chathura/


# Expose port 8132 to allow access to application
EXPOSE 8132

# Run the process in the background 
CMD ["java", "-jar", "/opt/chathura/chathura-product.jar"]