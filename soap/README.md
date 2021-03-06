#### JMeter Perfromance Tests for SOAP Web Services
This repository contains a simple test case to performance test a SOAP Web Service. For this test case the [calculator](http://www.dneonline.com/calculator.asmx) web service has been used.

Steps to execute the test case:

1. Launch Apache JMeter *GUI* and open the test: `Test_SOAP.jmx`. It sends a few SOAP requests to the calculator web service.
![SOAP Test: WSDL](https://github.com/techyugadi/jmeter_scripts/blob/master/img/jmeter14.png)
**SOAP Test: WSDL**
![SOAP Test: Operation](https://github.com/techyugadi/jmeter_scripts/blob/master/img/jmeter15.png)
**SOAP Test: Operation**
2. Run the test from the *GUI* and observe the results.
![SOAP Test Result](https://github.com/techyugadi/jmeter_scripts/blob/master/img/jmeter16.png)
**SOAP Test Results**

Later, the test should be performed through command-line, instead of the GUI.
