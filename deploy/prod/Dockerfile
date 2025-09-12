FROM node:24.8.0-trixie-slim as server

WORKDIR /app
COPY ./package.json ./
COPY ./yarn.lock ./
RUN yarn install

COPY . .

RUN yarn build

CMD ["node", "dist/main"]
