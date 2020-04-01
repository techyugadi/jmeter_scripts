#### JMeter Performance Tests with Grafana Dashboards
This repository contains a test case for performance testing a Java (Spring) Web application called Petclinic and produce real-time dashboards using Grafana.

The same set-up as in the web application test case, can be reused.

The test-case to be launched using Apache JMeter GUI is: `dashboard/Test_PetClinic.jmx`.

Additionally, the test-case uses a *Backend Listener* to store performance metrics in InfluxDB. A Grafana set-up connected to the InfluxDB backend will be able to produce *real-time* dashboards from these metrics.

For this purpose:
- A database named `jmeter` can be created in InfluxDB
- A Grafana datasource for the above database on InfluxDB can be configured
- Grafana dashboards can be created

Later, the test should be performed through command-line, instead of the GUI.
