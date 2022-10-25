# Build stage

FROM node:12

RUN apt install git wget
WORKDIR /src
RUN git clone https://github.com/mitre-attack/attack-navigator.git .

WORKDIR /src/nav-app

# give user permissions
RUN chown -R node:node ./

# install packages and build
RUN npm install --unsafe-perm

EXPOSE 4200

CMD npm start

USER node
