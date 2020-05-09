FROM node:12

# Also exposing VSCode debug ports
EXPOSE 8000

ENV ENABLE_GATSBY_REFRESH_ENDPOINT=true
ENV NODE_ENV=development

RUN npm install -g gatsby-cli

WORKDIR /app
COPY ./package.json .
RUN yarn install && yarn cache clean
COPY . .
CMD ["yarn", "develop", "-H", "0.0.0.0", "-p", "8000" ]

# FROM node:12 as builder
# WORKDIR /app

# USER root

# RUN npm install -g gatsby-cli
# ENV ENABLE_GATSBY_REFRESH_ENDPOINT true

# COPY ./package.json ./
# RUN npm install
# COPY ./ ./

# EXPOSE 8000
# CMD ["gatsby", "develop", "-p $PORT", "-H 0.0.0.0"]