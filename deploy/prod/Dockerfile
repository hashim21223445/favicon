FROM node:24.8.0-alpine3.22 as server

WORKDIR /app
COPY ./package.json ./
COPY ./yarn.lock ./
RUN yarn install

COPY . .

RUN yarn build

CMD ["node", "dist/main"]
