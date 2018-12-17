FROM node:8

# Create app directory
WORKDIR /usr/src/

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./

RUN npm install
# If you are building your code for production
# RUN npm install --only=production

ENV PATH /usr/src/node_modules/.bin:$PATH

# Bundle app source
COPY . /usr/src/app/

WORKDIR /usr/src/app/

EXPOSE 8080
CMD [ "npm", "start" ]
