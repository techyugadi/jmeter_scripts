#### JMeter Performance Tests for Web Applications
This repository contains a test case for performance testing a Java (Spring) Web application called Petclinic.

Steps to execute the test case:
1. A slightly modified version of the Spring Petclinic application is provided in the directory `webapp/setup/spring-petclinic`. Build this application: `cd webapp/setup/spring-petclinic; ./mvnw clean package -DskipTests=true`.
2. Copy the `petclinic.war` file generated under `webapp/setup/spring-petclinic/target` to the `compose` directory.
3. Start the Petclinic application using `docker-compose`: run `cd webapp/setup/compose; docker-compose up`.
4. Launch Apache JMeter *GUI* and open the test case: `webapp/test/Test_PetClinic.jmx`. This test case sends HTTP requests to various URLs in the Petclinic app for 3 minutes, simulating a load of 10 users.
![Test Case](https://github.com/techyugadi/jmeter_scripts/blob/master/img/jmeter01.png)
5. Observe the test results in the *GUI*.
![Response Times](https://github.com/techyugadi/jmeter_scripts/blob/master/img/jmeter02.png)
![Response Times (Graphical)](https://github.com/techyugadi/jmeter_scripts/blob/master/img/jmeter03.png)

Cleanup:

Note: the same set up can be used to run the JDBC performance test in this repository. So you may want to run those tests before cleaning up.

When the performance tests are completed, run: `cd webapp/setup/compose; docker-compose down; docker-compose rm`

##### Executing the Test Case from Command-line:
JMeter test case should NOT be run from the GUI, except to set it up for the first time and for familiarizing with the test case.

A slightly modified version of the test case (that does not produce test results within the GUI) is provided in the directory: `webapp/test/runcmd`.

To execute this test case from the command line, run:
`cd webapp/test/runcmd; mkdir -p raw output; <apache-jmeter-home>/bin/jmeter -n -t Test_PetClinic.jmx -J jmeter.reportgenerator.report_title=PetClinic_Performance -l raw/petclinic.jtl -e -o output`

The raw performance metrics are saved in the file `raw/petclinic.jtl` and HTML output is generated in `output` directory.

After completion of the test, to browse the test result, open the file `output/index.html` in a browser.

![Results Summary](https://github.com/techyugadi/jmeter_scripts/blob/master/img/jmeter05.png)
![Response Times (Graphical)](https://github.com/techyugadi/jmeter_scripts/blob/master/img/jmeter06.png)
