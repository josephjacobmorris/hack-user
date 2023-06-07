# 1. pick a node 11.13.0-alpine image
FROM node:11.13.0-alpine

# 2. create destination directory

WORKDIR /app

# 3. update and install dependency

COPY . /app
#COPY *.js /app
#COPY assets /app/assets
#COPY components /app/components
#COPY layouts /app/layouts
#COPY pages /app/pages
#COPY static /app/static
#COPY store /app/store

# 4. copy the app into the work directory and install packages needed for NodeJS

RUN npm install


# 5. build necessary, even if no static files are needed,

RUN npm run build
# since it builds the server as well

# 6. expose the port on container
EXPOSE 3000

# 7. set app serving to permissive / assigned

# 8. set app port

ENV NUXT_HOST=0.0.0.0
# 9. start the app
CMD npm start
