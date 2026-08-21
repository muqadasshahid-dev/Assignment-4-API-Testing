# Assignment 4 – API Testing

## 📌 Project Overview

This project contains the API functional and performance testing work completed for Assignment 4.

The testing was performed using **Postman** and **Apache JMeter** on the **JSONPlaceholder REST API**.

## 🛠️ Tools Used

- Postman – Functional API Testing
- Apache JMeter 5.6.3 – Performance and Load Testing
- JSONPlaceholder – REST API used for testing

## 🔗 API Under Test

Base URL:
<https://jsonplaceholder.typicode.com>

## 🧪 API Endpoints Tested

| Method | Endpoint   | Purpose                 |
| ------ | ---------- | ------------------------ |
| GET    | `/posts`   | Retrieve all posts      |
| GET    | `/posts/1` | Retrieve a single post  |
| POST   | `/posts`   | Create a new post       |
| PUT    | `/posts/1` | Update an existing post |
| DELETE | `/posts/1` | Delete a post           |

## ✅ Postman Testing Results

Automated tests were created to validate:

- HTTP status codes
- JSON response format
- Response structure
- Required fields
- ID and User ID
- Title and Body
- Updated data
- Response time

### Test Breakdown (per request)

| Request              | Automated Tests |
| -------------------- | ---------------- |
| GET - All Posts       | 9                |
| GET - Single Post     | 7                |
| POST - Create Post    | 9                |
| PUT - Update Post     | 7                |
| DELETE - Delete Post  | 3                |
| **Total**             | **35**           |

### Collection Runner Result

- **Total Tests:** 35
- **Passed:** 35
- **Failed:** 0
- **Skipped:** 0
- **Errors:** 0

## ⚡ JMeter Performance Testing

A load test was performed using Apache JMeter against all five CRUD requests.

### Test Configuration (Thread Group)

- Virtual Users (Threads): 10
- Ramp-Up Period: 5 seconds
- Loop Count: 5
- Samples per request: 50 (10 users × 5 loops)
- HTTP Header Manager: `Content-Type: application/json`

### Performance Results (Summary Report)

| API Request           | Samples | Average (ms) | Min (ms) | Max (ms) | Error % | Throughput |
| ---------------------- | ------- | -------------- | -------- | -------- | ------- | ----------- |
| GET - All Posts        | 50      | 67             | 22       | 354      | 0.00%   | 7.2/sec     |
| GET - Single Post      | 50      | 42             | 18       | 254      | 0.00%   | 7.4/sec     |
| POST - Create Post     | 50      | 255            | 238      | 455      | 0.00%   | 7.3/sec     |
| PUT - Update Post      | 50      | 0              | 0        | 0        | 100.00% | 7.7/sec     |
| DELETE - Delete Post   | 50      | 264            | 238      | 506      | 100.00% | 7.4/sec     |
| **TOTAL**              | 250     | 125            | 0        | 506      | 40.00%  | 33.5/sec    |

**Note:** GET and POST requests completed reliably with a 0% error rate. The PUT and DELETE
requests recorded a 100% error rate during this JMeter run, despite passing functional
validation in Postman. This discrepancy is noted as an open item — see `View Results Tree`
in JMeter (Response Data tab) for further investigation before treating PUT/DELETE as fully
verified under load.

## 📂 Repository Contents

```
Assignment-4-API-Testing/
│
├── README.md
├── API Testing Report.pdf
│
├── Postman/
│   ├── Assignment 4 - API Testing.postman_collection.json
│   ├── README.md
│   └── Screenshots for postman/
│
├── JMeter/
│   ├── API Testing - JSONPlaceholder.jmx
│   └── Screenshots for jmeter/
```

> Note: Previously this folder also contained `Summary Report.jmx` and `View Results Tree.jmx`,
> which were duplicate exports identical to `API Testing - JSONPlaceholder.jmx`. These, along
> with two empty stray files, have been removed for clarity.
