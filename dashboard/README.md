#### JMeter Performance Tests with Grafana Dashboards
This repository contains a test case for performance testing a Java (Spring) Web application called Petclinic and produce real-time dashboards using Grafana.

The same set-up as in the web application test case, can be reused.

The test-case to be launched using Apache JMeter GUI is: `dashboard/Test_PetClinic.jmx`.

Additionally, the test-case uses a *Backend Listener* to store performance metrics in InfluxDB. A Grafana set-up connected to the InfluxDB backend will be able to produce *real-time* dashboards from these metrics.

![Using Grafana](https://github.com/techyugadi/jmeter_scripts/blob/master/img/jmeter17.png)
**InfluxDB BackendListener**

For this purpose:
- A database named `jmeter` can be created in InfluxDB. Note: The InfluxDB backend listener expects the database name to be `jmeter`. \
  `CREATE DATABASE jmeter`
- A Grafana datasource for the above database on InfluxDB can be configured
![Datasource](https://github.com/techyugadi/jmeter_scripts/blob/master/img/jmeter18.png)
- Grafana dashboards can be created. An [example dashboard](https://github.com/techyugadi/jmeter_scripts/blob/master/dashboard/dashboard.json) is available in this repository. It produces graphs like the ones shown below:
![Dashboard](https://github.com/techyugadi/jmeter_scripts/blob/master/img/jmeter19.png)

Data for the dashboard is retrieved from InfluxDB. This can be verified by running the following commands on the InfluxDB shell:

```
use jmeter
 show measurements
```

![Queries](https://github.com/techyugadi/jmeter_scripts/blob/master/img/jmeter20.png)

The example dashboard can be imported into Graphana using Dashboard APIs, for example: \
`curl -X POST -H "Content-Type: application/json" -H "Authorization: Bearer $BEARER_TOKEN" -d @dashboard.json http://localhost:3000/api/dashboards/db`

Later, the test should be performed through command-line, instead of the JMeter GUI.
