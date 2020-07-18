FROM node:12

# Create app directory
WORKDIR /usr/src/app

# Copies source code over
COPY package*.json ./

# Installs dependencies
RUN npm ci

# Fixes known security vulnerabilities in container
RUN npm audit fix


# Bundle app source
COPY . .

EXPOSE 80

CMD [ "npm", "run", "prod" ]