FROM node:14.18.1-alpine

WORKDIR /usr/example/app
COPY package.json .
RUN npm install
COPY . .

RUN npm run build && \
    npm prune --production

EXPOSE 3000

ENTRYPOINT [ "node", "dist/server.js" ]