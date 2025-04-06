### 🚀 **Performance Testing**
## 📌 **Objective**
To evaluate the performance of the Restful Booker API using Apache JMeter under different load conditions, focusing on metrics such as response time, error rate, and system behavior under concurrent users.

## 🧪 **Tools & Frameworks**
-**Apache JMeter** – Performance testing tool

-**CSV Data Set Config** – For dynamic input of API endpoints/auth credentials

-**Restful Booker API** – https://restful-booker.herokuapp.com/apidoc/index.html

-**HTML Report** – For visualizing test results

## 🧾 **Test Plan Overview**
-**Authentication**: Handled via a CSV file (username.csv) containing valid tokens or credentials

-**API Coverage**: Includes endpoints like GET /booking, POST /booking, PUT /booking/{id}, DELETE /booking/{id}

-**Concurrency**: Tests are executed with varying numbers of concurrent users (e.g., 100, 500, 800, 1000, 1200)

-**Assertions**: To validate expected response codes and error messages

## 📁 **JMeter test plan file**: /performance/Performance_Testing_Project.jmx
## 📁 **API list & auth file**: /performance/username.csv

## ▶️ How to Run the Test
# jtl file-making command
```console
Copy
Edit
jmeter -n -t filename.jmx -l report\filename.jtl
```

# html file generate command
```console
Copy
Edit
jmeter -g report\filename.jtl -o report\filename.html
```
📈 **Metrics Collected**
Average Response Time:	Mean time taken for API responses
Max Response Time:	Highest observed response time
Requests per Second:	Throughput under load
Error Rate:	Percentage of failed API calls
Concurrent Users:	Number of simultaneous users simulated
## 📊 Sample Result Summary

| Users | Errors (%) | Avg TPS       | Total Concurrent Users |
|-------|------------|---------------|-------------------------|
| 100   | 0.00       | 44.3/sec      | 600                     |
| 500   | 0.00       | 197.5/sec     | 3000                    |
| 800   | 0.00       | 319.9/sec     | 4800                    |
| 1000  | 0.05       | 400.3/sec     | 6000                    |


## 📂 Reports
After execution, JMeter generates a detailed HTML report, including graphs and metrics:

## 📁 Output directory: /performance/reports/

Open index.html in any browser to view the report summary.

## 🧠 Observations
The API performs optimally under up to 800 users.

Slight increase in error rate and latency beyond 1000 concurrent users.

Authentication flow remains stable across all test loads.

📌 **Contributor**: Rupa Dey  
📅 **Last Updated**: 4th April, 2025
