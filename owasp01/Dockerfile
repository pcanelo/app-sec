FROM node:12
RUN apt update
RUN apt upgrade
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm install
COPY . .
ENV SESSION_SECRET=$(uuidgen)
EXPOSE 5000
CMD [ "node", "index.js" ]