FROM node:20
RUN mkdir /app 
WORKDIR /app
COPY *.json .
COPY *.js .
RUN npm install
CMD ["node","server.js"]