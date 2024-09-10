FROM node:22-alpine3.19
EXPOSE 3000
CMD npm run start:dev

RUN mkdir /home/node/jorge
WORKDIR /home/node/jorge
COPY ./proyecto-c/src /home/node/jorge/src
COPY ./proyecto-c/test /home/node/jorge/test
COPY ./proyecto-c/.eslintrc.js /home/node/jorge/.eslintrc.js
COPY ./proyecto-c/.gitignore /home/node/jorge/.gitignore
COPY ./proyecto-c/.prettierrc /home/node/jorge/.prettierrc
COPY ./proyecto-c/nest-cli.json /home/node/jorge/nest-cli.json
COPY ./proyecto-c/package.json /home/node/jorge/package.json
COPY ./proyecto-c/README.md /home/node/jorge/README.md
COPY ./proyecto-c/tsconfig.build.json /home/node/jorge/tsconfig.build.json
COPY ./proyecto-c/tsconfig.json /home/node/jorge/tsconfig.json
USER root
RUN npm install
RUN apk update && apk add wget