FROM maven:3.9.16
RUN mkdir /app
WORKDIR /app
COPY pom.xml .
COPY src /app/src
RUN mvn clean package
RUN mv target/shipping-1.0.jar shipping.jar
EXPOSE 8080
CMD ["java","-jar","shipping.jar"]
