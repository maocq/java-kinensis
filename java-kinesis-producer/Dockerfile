#FROM ibm-semeru-runtimes:open-17.0.7_7-jre-jammy
#WORKDIR /app
#COPY . .
#RUN ./gradlew bootJar

FROM ibm-semeru-runtimes:open-17.0.7_7-jre-jammy
WORKDIR /app
COPY JavaKinesis.jar app.jar

ENV JAVA_OPTS="-XX:+UseContainerSupport"
ENTRYPOINT ["sh","-c","java $JAVA_OPTS -jar app.jar"]