# qa-backend-automation

Example of API tests using Apache Jmeter


## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)


## General info
This project is a simple use case of jmeter on functional behaviour testing (Dummy API on http://dummy.restapiexample.com/ )

### WARNING
This dummy API, as informed, does not provide consistent responses:
* supposedly deleted users can be queried (after "successful" DELETE)
* can't get user information after test creation (only id is returned, when trying to GET user information)
* documentation also have inconsistencies (to delete a user, both GET and DELETE http methods could be used, according information on different pages)
	

## Setup

* Install Apache JMeter 5.3 (Requires Java 8+) -  https://jmeter.apache.org



### Tips:

* The dummy API on dummy.restapiexample.com presents 'HTTP 429 (Too many requests)' responses even if your request rate is 2 per minute or less :-(  
* Used Constant Throughput Timer to control interval between requests 


### How to run


* Start Jmeter according to your OS:

jmeter.bat (Windows)

OR

jmeter.sh (Linux/MacOS)


* Open the file: "dummy_api_tests.jmx"

* Click on Start button (or Run / Start) and use "View Results Tree" element on the bottom of the Test Plan to check results of the tests