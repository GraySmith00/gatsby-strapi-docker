FROM node:12

# Also exposing VSCode debug ports
EXPOSE 8000 9929 9230

ENV ENABLE_GATSBY_REFRESH_ENDPOINT=true
ENV NODE_ENV=development

WORKDIR /gatsby-app

RUN npm install -g gatsby-cli

COPY ./package.json .
RUN yarn install && yarn cache clean
COPY . .

RUN ls -l

CMD ["gatsby", "develop", "-H", "0.0.0.0", "-p", "8000" ]