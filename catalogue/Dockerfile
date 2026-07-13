FROM node:20
RUN mkdir /app 
WORKDIR /app
COPY *.json .
COPY *.js .
RUN npm install
ENV MONGO="true" \
    MONGO_URL="mongodb://mongo:27017/catalogue"
CMD ["node","server.js"]