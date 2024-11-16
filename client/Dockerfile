FROM node:alpine

# create-react-app currently has 2 bugs that prevent it from running correctly in a docker container
# so, add those 2 lines
ENV CI=true
ENV WDS_SOCKET_PORT=0

WORKDIR /app
COPY package.json ./
RUN npm install
COPY ./ ./

CMD [ "npm", "start" ]