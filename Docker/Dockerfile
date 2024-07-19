FROM node:20.9.0-alpine

WORKDIR /usr/src/app

COPY package*.json .

RUN npm install

COPY . .

EXPOSE 3000

CMD ["node", "index.js"]


# Whenever a layer changes(means changes in code/file), that layer will need to be re-built.
# All the above layers of the changed layer will be cached and won't be re-built.
# All the below layers and the changed layer will be re-built as changes were detected in current layer.

# We first copy over package.json and package-lock.json, run npm install followed by copying over the code
# This way, the layer which runs npm install can be cached until package.json isn't changed, which doesn't happen very often in the lifecycle of a project

# Use the alpine-node image which is much more lightweight than the node image, so that the size of the image will be light.





# Multi stage builds

FROM node:20 AS base
WORKDIR /usr/src/app
COPY package*.json .
RUN npm install

FROM base AS development
COPY . .
CMD ["npm", "run", "dev"]

FROM base AS production
COPY . .
RUN npm prune --production
CMD ["npm", "run", "start"]

# Building dev:
# docker build --target development -t myapp:dev .

# Building prod:
# docker build --target production -t myapp:prod .

