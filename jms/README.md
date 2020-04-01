#### JMeter Performance Tests for JMS
This repository contains a simple test case for performance-testing a JMS broker like ActiveMQ.

Steps to execute the test case:

1. Launch a JMS broker like ActiveMQ. For example, we can run ActiveMQ in a docker: `docker run --name='activemq' -it --rm -p 8161:8161 -p 61616:61616 -p 61613:61613 webcenter/activemq:latest`
2. Download a suitable JMS client and copy it to `lib` directory in your Apache JMeter installation, for example: [ActiveMQ JMS client](https://repo1.maven.org/maven2/org/apache/activemq/activemq-all/5.15.12/activemq-all-5.15.12.jar)
3. Launch Apache JMeter *GUI* and open the test: `Test_JMS.jmx`. It sends a few text messages to a dynamic queue on ActiveMQ.
4. Run the test from the *GUI* and observe the results.

Later, the test should be performed through command-line, instead of the GUI.
