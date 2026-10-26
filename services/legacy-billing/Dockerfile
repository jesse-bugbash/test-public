FROM openjdk:8-jre-alpine
MAINTAINER billing@example.com
ADD target/billing.war /opt/billing/billing.war
WORKDIR /opt/billing
EXPOSE 8080
CMD java -jar billing.war
