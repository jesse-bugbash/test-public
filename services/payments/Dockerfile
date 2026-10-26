FROM maven:3.9-eclipse-temurin-21 AS build
WORKDIR /build
COPY pom.xml .
RUN mvn -B dependency:go-offline
COPY src ./src
RUN mvn -B package -DskipTests

FROM eclipse-temurin:21-jre-jammy
LABEL org.opencontainers.image.title="payments" \
      org.opencontainers.image.vendor="Example Shop" \
      org.opencontainers.image.licenses="Apache-2.0"

RUN useradd --system --uid 10001 payments
WORKDIR /opt/payments
COPY --from=build /build/target/payments-*.jar app.jar
USER payments
EXPOSE 8443
ENTRYPOINT ["java", "-XX:MaxRAMPercentage=75", "-jar", "app.jar"]
