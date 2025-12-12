# base image
FROM mysql:8.0

# set working directory
WORKDIR /docker-entrypoint-initdb.d

# copy initialization script
COPY init.sql /docker-entrypoint-initdb.d/

# set environment variables 
ENV MYSQL_ROOT_PASSWORD=root
