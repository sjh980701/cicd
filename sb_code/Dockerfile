FROM maven:3.6.3-openjdk-8-slim AS builder
WORKDIR /app
COPY . .
RUN mvn clean package

FROM openjdk:8-alpine
WORKDIR /app
COPY --from=builder /app/target/springbootApp.jar app.jar
CMD ["java","-jar","app.jar"]

 
