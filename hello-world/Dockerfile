FROM eclipse-temurin:21-jdk AS build
WORKDIR /app
COPY src/Main.java .
RUN javac -d out Main.java

FROM eclipse-temurin:21-jre
WORKDIR /app
COPY --from=build /app/out .
EXPOSE 8080
CMD ["java", "hello.Main"]
