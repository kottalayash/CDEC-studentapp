FROM maven:3.8.5-openjdk-17

COPY . /app
WORKDIR /app

RUN mvn clean package 
EXPOSE 8080
CMD ["java", "-jar", "target/*.jar"]
