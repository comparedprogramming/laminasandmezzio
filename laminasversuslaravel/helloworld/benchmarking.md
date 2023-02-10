# Benchmarking: comparing Hello, World in Laminas and Laravel

The performance test results below were obtainer with Apache JMeter using a PHP web server 8.1

**Laminas**

```bash
Generate Summary Results =  10000 in 00:00:34 =  295.9/s Avg: 13443 Min:   142 Max: 24886 Err:     0 (0.00%)
```

**Laravel**

```bash
Generate Summary Results =  10000 in 00:01:15 =  132.7/s Avg: 34014 Min:  1013 Max: 67137 Err:     0 (0.00%)
```

You can use .jmx files to reproduce the tests with any web server. There is a .jmx file for each framework.

## How to Install Apache JMeter in a Debian distro

Change the version number for desirable version.

```bash
apt-get install --yes openjdk-11-jdk

apt-get install --yes wget 

wget https://dlcdn.apache.org//jmeter/binaries/apache-jmeter-5.5.zip

apt-get install --yes unzip 

unzip apache-jmeter-5.5.zip

mv apache-jmeter-5.5 apache-jmeter
```

After the installation, you can run a test plan this way:

```bash
RUN apache-jmeter/bin/jmeter -n -t [filename].jmx
```