# Spring Boot JPA Driven Test Harness

### Introduction

Using JPA to push data into a mysql database. 
Update application.yml to configure the external database.

The route is set on a timer so data is pushed into database automatically as soon as the camel route is started


### Build

You can build this example using:

```sh
$ mvn package
```

### Run

You can run this example with Maven using:

```sh
$ mvn spring-boot:run 
```

Alternatively, you can also run this example using the executable JAR:

```sh
$ java -jar target/camel-example-spring-boot-rest-jpa-${project.version}.jar
```

When the Camel application runs, you should see the following messages
being logged to the console, e.g.:

```
2016-09-02 09:54:29.702  INFO 27253 --- [mer://new-order] generate-order : Inserted new order 1
2016-09-02 09:54:31.597  INFO 27253 --- [mer://new-order] generate-order : Inserted new order 2
2016-09-02 09:54:33.596  INFO 27253 --- [mer://new-order] generate-order : Inserted new order 3
2016-09-02 09:54:34.637  INFO 27253 --- [rts.camel.Order] process-order  : Processed order #id 1 with 7 copies of the «Camel in Action» book
2016-09-02 09:54:34.641  INFO 27253 --- [rts.camel.Order] process-order  : Processed order #id 2 with 4 copies of the «Camel in Action» book
2016-09-02 09:54:34.645  INFO 27253 --- [rts.camel.Order] process-order  : Processed order #id 3 with 1 copies of the «ActiveMQ in Action» book
2016-09-02 09:54:35.597  INFO 27253 --- [mer://new-order] generate-order : Inserted new order 4
2016-09-02 09:54:37.601  INFO 27253 --- [mer://new-order] generate-order : Inserted new order 5
2016-09-02 09:54:39.605  INFO 27253 --- [mer://new-order] generate-order : Inserted new order 6
2016-09-02 09:54:39.668  INFO 27253 --- [rts.camel.Order] process-order  : Processed order #id 4 with 7 copies of the «Camel in Action» book
2016-09-02 09:54:39.671  INFO 27253 --- [rts.camel.Order] process-order  : Processed order #id 5 with 1 copies of the «ActiveMQ in Action» book
2016-09-02 09:54:39.674  INFO 27253 --- [rts.camel.Order] process-order  : Processed order #id 6 with 4 copies of the «Camel in Action» book
```

You can then access the REST API directly from your Web browser, e.g.:

- <http://localhost:8080/camel-rest-jpa/books/order/1>

The Camel application can be stopped pressing <kbd>ctrl</kbd>+<kbd>c</kbd> in the shell.

### Swagger API

The example provides API documentation of the service using Swagger using
the _context-path_ `camel-rest-jpa/api-doc`. You can access the API documentation
from your Web browser at <http://localhost:8080/camel-rest-jpa/api-doc>.
