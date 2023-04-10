FROM node:14-alpine as builder 

LABEL Maintainer Magda 

RUN mkdir /app 

WORKDIR /app 

ENV NODE_ENV=production 

COPY package.json /app/ 
COPY package-lock.json /app/ 

RUN npm install 

COPY . /app/ 

RUN npm run build 

RUN npm install -g serve 

FROM gcr.io/distroless/nodejs18-debian11 

COPY --from=builder /app /app 

WORKDIR /app 

EXPOSE 4000

CMD [ "serve", "-s", "build", "-l", "4000" ]