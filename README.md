# Assignment No. 4 – API Testing

## Objective

The objective of this assignment is to perform API testing using **JSONPlaceholder**.

The assignment includes:

1. API functional testing using Postman.
2. Basic performance testing using Apache JMeter.
3. Analysis of response time, throughput, and error rate.
4. Uploading the required testing artifacts to GitHub.

---

## API Under Test

**API:** JSONPlaceholder

JSONPlaceholder is a free fake REST API used for testing and development.

---

# Part 1 – Postman API Testing

Postman was used to perform functional validation of the API.

### Testing Performed

The API request was sent through Postman and the response was checked for:

- HTTP status code
- Response body
- Response data
- API response correctness

### Expected Result

The API should return a successful HTTP response and valid JSON data.

### Postman Collection

The Postman collection JSON file is included in this repository.

---

# Part 2 – Apache JMeter Performance Testing

Apache JMeter was used to perform basic performance testing of the API.

## JMeter Test Plan

The following components were created:

## JMeter Test Plan includes:

-Thread Group
-HTTP Request
-View Results Tree
-Summary Report

## Thread Group Configuration

The Thread Group was configured with:

| Setting | Value |
|---|---:|
| Number of Threads (Users) | 10 |
| Ramp-Up Period | 5 seconds |
| Loop Count | 5 |
| Total Requests | 50 |

### HTTP Request

An HTTP Request sampler was configured to send a GET request to the JSONPlaceholder API.

- Protocol: HTTPS
- Server: jsonplaceholder.typicode.com
- Path: /posts
- Method: GET

### View Results Tree

The View Results Tree listener was used to inspect individual API responses, including response status, response body, and response time.

### Summary Report

The Summary Report was used to analyze the overall performance of the API.

| Metric | Result |
|---|---:|
| Samples | 50 |
| Average Response Time | 1415 ms |
| Minimum Response Time | 136 ms |
| Maximum Response Time | 24344 ms |
| Error Rate | 0.00% |
| Throughput | 1.0/sec |

### Results Analysis

The test completed 50 samples with an error rate of 0.00%, meaning all requests were successfully completed.

The average response time was 1415 ms. The minimum response time was 136 ms, while the maximum response time was 24344 ms.

The observed throughput was approximately 1 request per second.

## Repository Contents

The repository contains:

- Postman Collection JSON file
- JMeter Test Plan (.jmx)
- JMeter Results Screenshot
- README.md
## How to Run the Tests

### Postman
1. Import the Postman Collection JSON file.
2. Open the collection.
3. Run the API requests or use Collection Runner.
4. Check the automated test results.

### JMeter
1. Open the `.jmx` test plan in Apache JMeter.
2. Verify the Thread Group settings.
3. Run the test.
4. Open the Summary Report to view performance results.

## Conclusion

The JSONPlaceholder API was successfully tested using Postman for functional API validation and Apache JMeter for basic performance testing.

The JMeter test was performed using 10 users, a 5-second ramp-up period, and 5 loops. The test completed 50 samples with a 0.00% error rate.

## Tools Used

- Postman
- Apache JMeter
- JSONPlaceholder
- GitHub

## Author
-LAIBA
