FROM maven:3
RUN mkdir /app
WORKDIR /app
RUN mvn clean package && mv target/shipping-1.0.jar shipping.jar
CMD ["java","-jar","shipping.jar"]
