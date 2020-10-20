FROM node:8

WORKDIR /mydir
RUN apt-get update && apt-get install -y curl git
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get update && apt-get install -y nodejs
RUN git clone https://github.com/jooala/woltsummer2020

EXPOSE 3000
WORKDIR /mydir/woltsummer2020
ENV BROWSER=none

RUN rm -rf node_modules
RUN npm cache clear --force
RUN npm install
CMD npm start
