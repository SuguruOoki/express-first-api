FROM node:16

COPY ./src /app
WORKDIR /app
RUN yarn add --dev yarn-upgrade-all
RUN yarn yarn-upgrade-all && yarn audit fix --force
RUN yarn add -g db-migrate db-migrate-mysql
RUN db-migrate up
