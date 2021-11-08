FROM node:14 as build-env 

WORKDIR /usr/src/app

COPY . .

FROM node:14-alpine

WORKDIR /usr/src/app

COPY --from=build-env /usr/src/app /usr/src/app

ENV REACT_APP_BACKEND_URL=http://localhost:8080/

RUN npm install && \
npm run build  && \
npm install -g serve

CMD serve -s -l 5000 build
