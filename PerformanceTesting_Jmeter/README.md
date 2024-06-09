# Performance Testing
This repository contains performance testing documentation to evaluate the performance of the Restful Booker API hosted on restful-booker.herokuapp.com. The tests are conducted using Apache JMeter, a powerful open-source tool for performance testing.
## Install
JAVA

https://www.oracle.com/java/technologies/downloads/

JMeter

https://jmeter.apache.org/download_jmeter.cgi

## Collection of API

A set of API for restful-booker.herokuapp.com is utilized, which includes various HTTP methods such as POST, GET, DELETE, and PUT.

## Load Testing

## Test Plan
Test Plan > Add > Threads (Users) > Thread Group

Name: Users

Number of Threads (Users): 

Ramp-up Periods (in Seconds):

Loop Count: 1


1. Test Plan specifies the general settings for test execution, such as whether Thread Groups will run simultaneously or sequentially.
2. HTTP Requests utilize some of the HTTP Request item's default settings, such as the Server IP, Port Number, and Content-Encoding.
3. Each Thread Group describes how HTTP requests should be executed. To establish how many concurrent "users" will be simulated, we first need to determine the number of threads. The loop count determines the number of actions that each "user" will perform.
4. The first item in Thread Groups is the HTTP Header Manager, which lets you input the Request Headers that the next HTTP Requests will use.

## First Thread Group


Number of Threads: 100

Ramp-up Period:1



![report_1](https://github.com/FarhanaAntora/PerformanceTesting_Jmeter/assets/96485899/907e797f-2acb-4bf6-9d64-513460ff1ccc)

## Second Thread Group

Number of Threads: 1600

Ramp-up Period: 1



![report_2](https://github.com/FarhanaAntora/PerformanceTesting_Jmeter/assets/96485899/478cdf78-37ed-44f6-86a7-add9053e0c5e)


## Third Thread Group

Number of Threads: 2500

Ramp-up Period: 1



![report_3](https://github.com/FarhanaAntora/PerformanceTesting_Jmeter/assets/96485899/4a31705d-e04b-4d09-b102-3bf7bede24af)


## Summary 

While executed 100 Threads, a total of 600 concurrent request are made found with error rate 0%

While executed 1600 Threads, a total of 9600 concurrent request are made found with error rate 0%

While executed 2500 Threads, a total of 15000 concurrent request are made found with error rate 0.02%


Server can handle almost concurrent 2500 API call with almost zero error rate.




