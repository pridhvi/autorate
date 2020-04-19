FROM maven AS builder

COPY . /autorate

WORKDIR /autorate

RUN mvn clean install

FROM java:8

COPY --from=builder /autorate/target/autorate-*.jar /autorate/autorate.jar

CMD java -jar /autorate/autorate.jar