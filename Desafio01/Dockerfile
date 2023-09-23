FROM 3.9.4-eclipse-temurin-17 as build

WORKDIR /app

COPY pom.xml .
RUN mvn dependency:go-offline

COPY src ./src
RUN mvn package

FROM openjdk:17-jre-centos7

COPY --from=build /app/target/Desafio01.jar /app/app.jar

EXPOSE 8080

CMD ["java", "-jar", "/app/app.jar"]
