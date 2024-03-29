FROM node:18
# #Create a working directory
WORKDIR /usr/src/app
#Install app-dependencies
COPY package.*json ./
RUN npm install
RUN npx prisma generate
COPY . .
EXPOSE 5001
CMD [ "node", "server.js"]