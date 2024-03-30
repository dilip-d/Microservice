FROM node:18
#Create a working directory
WORKDIR /usr/src/app
#Install app-dependencies
COPY package.*json ./
RUN npm install
COPY prisma ./prisma/
RUN npx prisma generate
COPY . .
# RUN docker compose up 
# RUN npx prisma migrate dev
EXPOSE 5002
CMD [ "node", "server.js"]
