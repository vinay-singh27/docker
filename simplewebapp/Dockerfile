# specify the base
FROM node:alpine 

WORKDIR /usr/app

# copy the dependecies
COPY ./package.json ./
RUN npm install

# run the dependecies
COPY ./ ./

# run the start command
CMD ["npm", "start"]