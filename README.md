📄 RESTBooker API Test Documentation
🧪 Test Summary
API Name: RESTBooker

Tool Used: Apache JMeter

Test Plan Source: restbooker_test_plan.jmx

Report Format: HTML (auto-generated from JMeter run)

Test Date: 14th march 2025

Tester: Rupa Dey

🔧 Test Configuration
Thread Groups:

Total Threads (Users): 100

Ramp-up Period: 3010 seconds

Loop Count: 1 

Base URL:https://restful-booker.herokuapp.com/apidoc/index.html#

🧵 Test Scenarios
Create Booking

Method: POST

Edit
{
  {
    "firstname" : "Dola",
    "lastname" : "Dey",
    "totalprice" : 12202,
    "depositpaid" : true,
    "bookingdates" : {
        "checkin" : "2024-01-01",
        "checkout" : "2026-01-01"
    },
    "additionalneeds" : "Biriyani"
}
Expected Status Code: 200 / 201

Get Booking

Method: GET

Endpoint: /booking/{id}

Expected Status Code: 200

Update Booking

Method: PUT

Authorization: Basic Auth (admin credentials)

Expected Status Code: 200

Delete Booking

Method: DELETE

Authorization: Basic Auth

Expected Status Code: 201

📈 Performance Metrics (From HTML Report)
Average Response Time: 230 ms

Max Response Time: 950 ms

Min Response Time: 120 ms

Throughput: 15 requests/sec

Error Rate: 0.00%

📋 Assertions
Response Code: Must be 200 / 201 for success

Response Time: Should be under 1s

Response Body: Must contain booking ID and other expected fields

🧼 Cleanup
Delete any bookings created during the test via DELETE /booking/{id}

📎 Attachments
HTML Report: performance_Testing_project.html

Test Plan File: Performance_Testing_Project.jmx








