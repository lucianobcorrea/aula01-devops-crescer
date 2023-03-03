FROM alpine
WORKDIR /app
COPY . /app
RUN npm install

FROM node:latest
COPY --from=build app/ /src/app
ENTRYPOINT [ "node", "server.js" ]
