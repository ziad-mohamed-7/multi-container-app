# base image
FROM node:slim

# set working directory
WORKDIR /app

# copy first for caching
COPY package.json .

# install dependencies in container
RUN npm install

# copy all files
COPY . .

# port to expose
EXPOSE 5173

# start server with host binding to allow external access
CMD ["npm", "run", "dev", "--", "--host"]