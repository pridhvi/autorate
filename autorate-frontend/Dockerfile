FROM maven AS builder

COPY . /autorate

WORKDIR /autorate

RUN mvn clean install

FROM tomcat:8.5

COPY --from=builder /autorate/target/autorate-*.war /usr/local/tomcat/webapps/
