# Project title: Load and Stress Testing University API
## Overview:
This project aims to determine the actual transactions per second (TPS) for the URL: https://webdriveruniversity.com/ and to identify the bottleneck point at which the system starts showing a 1% error rate under load. The project involves two primary tasks:
 - Calculating the actual TPS under a load of 120,000 users over 12 hours.
 - Conducting a stress test to find the point where the system begins to show a 1% error rate.
 - Find the capacity testing value.

## Prerequisites:
- Java (JDK 8 or above)
- Apache JMeter (version 5.0 or above)
- Excel

## Installation:
 - Install Java: Ensure that JDK 8 or above is installed on the system or downloaded from the java official website
 - Install Apache JMeter: Visit the Apache JMeter website and download the latest version of JMeter.Follow the installation instructions provided in the JMeter documentation for the operating system.
 - Setup JMETER_HOME and path

## Running JMeter:
 - Change to the bin directory 
 - Run the jmeter (Un*x) or jmeter.bat (Windows) file.
 - Creating The JMX file:
 - Follow the steps and create JMX file for the given scenario:

## Open JMeter: 
Launch JMeter and open the .jmx files located in the project directory.

## Create Test Plan:

-  After opening jmeter create a new test plan
- add Thread Group: add > threads (users) > Thread Group
- set the no of threads and ramp-up period and loop count

## Add HTTP Requests:

- Right-click on the thread group: Add->Sampler->HTTTP Request
- set the method as POST
- set the PATH
- Add a listener to see the result

## Run Tests:
Execute the test plan to simulate user activity and collect performance data.

## Load Test Analysis: 
- Simulate load on the API.
- Calculate expected and actual TPS.
- Record the results on an Excel sheet.

## Expected TPS Calculation

   - Total Users: 120,000
   - Test Duration: 12 hours (43,200 seconds)
   - Expected TPS: 120000/43200≈2.78


## Result analysis: 
The actual TSP and the Expected TSP are the same so the system is successful in the load test and ready for the stress test.

## Excel for Load Test :
![My Image](![image](https://github.com/Bonosree/Random-User-API-Performance-Test/assets/59661684/059af423-08d5-4d5d-89e5-16f3e07a252c)
)

## Stress Test Analysis
 - Incremental Load Increase
 - Start with a low number of users.
 - Gradually increase the number of users.
 - Monitor response times and error rates.
 - Identify Bottleneck Point
 - Identify the point at which error rate exceeds 1%.
 - Record the data and save it to an Excel sheet.

## Excel for stress test :
![My Image](![image](https://github.com/Bonosree/Random-User-API-Performance-Test/assets/59661684/b3f522b1-b1ed-439d-b41b-86d2609ae983)
)




















