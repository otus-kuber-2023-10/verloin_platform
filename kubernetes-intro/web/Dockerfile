# Set the base image to Ubuntu 
FROM ubuntu:20.04

# Update the repository
RUN apt-get update

# Install necessary tools
# ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get install dnsutils nano wget curl -y

# Download and install NGINX
RUN apt-get install nginx -y  

# Remove the default NGINX configuration file
# RUN rm -v /etc/nginx/nginx.conf

# Copy a configuration file from the current directory
COPY nginx.conf /etc/nginx/nginx.conf

RUN mkdir /app
COPY ./homework.html /app

# Expose ports
EXPOSE 8000

CMD ["nginx", "-g", "daemon off;"]