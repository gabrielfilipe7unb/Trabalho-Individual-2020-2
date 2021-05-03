# reference = https://github.com/nikolaik/docker-python-nodejs

FROM nikolaik/python-nodejs:latest

WORKDIR /client

COPY package.json ./

RUN yarn install

RUN yarn global add @quasar/cli 

COPY . .

EXPOSE $CLIENT_PORT 

CMD quasar dev