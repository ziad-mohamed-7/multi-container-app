# base image
FROM node:slim

# set working directory
WORKDIR /app

# install dependencies
RUN npm install express mysql2 cors body-parser csv-writer

# copy application file
COPY server.js .

# expose port
EXPOSE 3000

# start the server
CMD ["node", "server.js"]