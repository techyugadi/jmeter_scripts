#### JMeter Performance Tests for JDBC
This repository contains a simple test case for performance-testing a database connection using JDBC.

Steps to execute the test case:

1. For this test, we should use the same set-up that as in the Web Application example (Java Petclinic). Launch this web application using `docker-compose`.
2. Download *MySQL JDBC client* from maven repository and copy it to `lib` directory in your Apache JMeter installation: [MySQL JDBC Client](https://repo1.maven.org/maven2/mysql/mysql-connector-java/8.0.19/mysql-connector-java-8.0.19.jar)
3. Launch Apache JMeter *GUI* and open the test: `Test_MySQL.jmx`. It runs a few SQL queries on MySQL / MariaDB. The database is already populated with data for the Petclinic application.
![JDBC Test](https://github.com/techyugadi/jmeter_scripts/blob/master/img/jmeter04.png) 
![JDBC Test Results](https://github.com/techyugadi/jmeter_scripts/blob/master/img/jmeter05.png) 
4. Run the test from the *GUI* and observe the results.

Later, the test should be performed through command-line, instead of the GUI.
