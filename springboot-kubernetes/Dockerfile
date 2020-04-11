FROM adoptopenjdk/openjdk11:alpine-jre
ADD target/springboot-example.jar app.jar
ENTRYPOINT ["java","-jar","app.jar"]