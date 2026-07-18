FROM node:20.20.2-alpine3.22 AS builder
WORKDIR /app
COPY *.json .
COPY *.js .
RUN npm install



FROM node:20.20.2-alpine3.22
WORKDIR /app
EXPOSE 8080
RUN addgroup -S roboshop && adduser -S -G roboshop -h /home/roboshop -s /sbin/nologin roboshop && \ 
    chown -R roboshop:roboshop /app
copy --from=builder /app .
user roboshop
CMD ["node","server.js"]


# FROM node:20
# RUN mkdir /app 
# WORKDIR /app
# COPY *.json .
# COPY *.js .
# RUN npm install
# EXPOSE 8080
# CMD ["node","server.js"]