#### JMeter Perfromance Tests
This repository contains a set of tests to try out various features of Apache JMeter Performance Testing tool, particularly:
- [Web Applications (HTTP request-response)](https://github.com/techyugadi/jmeter_scripts/tree/master/webapp)
- [JDBC](https://github.com/techyugadi/jmeter_scripts/tree/master/jdbc)
- [JMS](https://github.com/techyugadi/jmeter_scripts/tree/master/jms)
- [MQTT](https://github.com/techyugadi/jmeter_scripts/tree/master/mqtt)
- [SOAP Web Service](https://github.com/techyugadi/jmeter_scripts/tree/master/soap)
- [Creating dashboards with Grafana (using InfluxDB for storing test metrics)](https://github.com/techyugadi/jmeter_scripts/tree/master/dashboard)

A slightly modified version of the Java Petclinic Application is bundled here, along with docker-compose artifacts to launch this application on:
- Tomcat Application Server with MariaDB as database and Nginx reverse-proxy

Commands to run JMS and MQTT in docker containers for the respective test cases, are also documented.
