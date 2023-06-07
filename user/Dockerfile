# 1. pick a Node 16 image
FROM node:16-alpine

# 2. set a working directory
WORKDIR /app

# 3. declare all the environemnt variables needed

ENV DATABASE_HOST=localhost
ENV DATABASE_PORT=5432
ENV DATABASE_NAME=public
ENV DATABASE_USERNAME=postgres
ENV DATABASE_PASSWORD=foo
ENV CONFIG_FILES_PATH=/

# 4. copy the app into the work directory

COPY src /app/src
COPY *.json /app
COPY *.js /app


# 5. install all the packages needed for NodeJS

RUN npm install

# 6. expose the port needed

EXPOSE 3000

# 7. start the app

CMD npm run start
