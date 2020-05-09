FROM node:12

# Also exposing VSCode debug ports
EXPOSE 1337

WORKDIR /strapi-app

COPY ./package.json .
RUN yarn install && yarn cache clean
COPY . .

RUN ls -l

CMD ["yarn", "develop"]