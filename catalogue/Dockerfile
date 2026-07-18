FROM node:20.20.2-alpine3.22 AS builder 
WORKDIR /app
COPY *.json .
COPY *.js .
RUN npm install
# CMD ["node","server.js"]

FROM node:20.20.2-alpine3.22
WORKDIR /app
EXPOSE 8080
RUN addgroup -S roboshop && adduser -S -G roboshop -h /home/roboshop -s /sbin/nologin roboshop && \ 
    chown -R roboshop:roboshop /app
COPY --from-builder /app /app   
USER roboshop      
CMD ["node","server.js"]



# FROM node:20
# RUN mkdir /app ( optional if not work WORKDIR will create)
# WORKDIR /app
# COPY *.json .
# COPY *.js .
# RUN npm install
# ENV MONGO="true" \
#     MONGO_URL="mongodb://mongo:27017/catalogue"
# CMD ["node","server.js"]