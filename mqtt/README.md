#### JMeter Performance Tests for MQTT
This repository contains a simple test case for performance-testing a MQTT broker like Mosquitto.

Steps to execute the test case:

1. Copy the following JMeter MQTT plugin to the `lib/ext` directory of your Apache JMeter installation: [JMeter MQTT Plugin](https://github.com/emqtt/mqtt-jmeter/releases). Once the plugin is installed, the MQTT menu items will be visible.
2. Launch an MQTT broker like Mosquitto. For example, we can run Mosquitto in a docker: `docker run -it --rm -p 1883:1883 -p 9001:9001  eclipse-mosquitto`
3. Launch Apache JMeter *GUI* and open the test: `Test_MQTT.jmx`. It sends a few messages (events) to Mosquitto broker.
![MQTT Test](https://github.com/techyugadi/jmeter_scripts/blob/master/img/jmeter11.png)
**MQTT Test**
![MQTT Connection](https://github.com/techyugadi/jmeter_scripts/blob/master/img/jmeter12.png)
**MQTT Connection**
4. Run the test from the *GUI* and observe the results.
![MQTT Test Result](https://github.com/techyugadi/jmeter_scripts/blob/master/img/jmeter13.png)
**MQTT Test Results**

Later, the test should be performed through command-line, instead of the GUI.

