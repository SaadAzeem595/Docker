FROM node

ENV MONGO_DB_USERNAME=admin \
    MONGO_DB_PWD=qwerty

RUN mkdir -p my-test-app

COPY . /my-test-app

CMD ["node", "/my-test-app/server.js"]


