#### JMeter Perfromance Tests
This repository contains a set of tests to try out various features of Apache JMeter Performance Testing tool, particularly:
- Web Applications (HTTP request-response)
- JDBC
- JMS
- MQTT
- SOAP Web Service
- Creating dashboards with Grafana (using InfluxDB for storing test metrics)

A slightly modified version of the Java Petclinic Application is bundled here, along with docker-compose artifacts to launch this application on:
- Tomcat Application Server with MariaDB as database and Nginx reverse-proxy

Commands to run JMS and MQTT in docker containers for the respective test cases, are also documented.
