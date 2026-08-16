
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

https://jsonplaceholder.typicode.com

## 🧪 API Endpoints Tested

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/posts` | Retrieve all posts |
| GET | `/posts/1` | Retrieve a single post |
| POST | `/posts` | Create a new post |
| PUT | `/posts/1` | Update an existing post |
| DELETE | `/posts/1` | Delete a post |

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

### Collection Runner Result

- **Total Tests:** 26
- **Passed:** 26
- **Failed:** 0
- **Skipped:** 0
- **Errors:** 0

## ⚡ JMeter Performance Testing

A basic load test was performed using Apache JMeter.

### Test Configuration

- Virtual Users: 10
- Ramp-Up Period: 5 seconds
- Loop Count: 5
- Total Samples: 50

### Performance Results

| Metric | Result |
|---|---:|
| Total Samples | 50 |
| Average Response Time | 118 ms |
| Minimum Response Time | 21 ms |
| Maximum Response Time | 1832 ms |
| Standard Deviation | 280.98 ms |
| Error Rate | 0.00% |
| Throughput | 10.6 requests/sec |

## 📂 Repository Contents

```text
Assignment-4-API-Testing/
│
├── README.md
├── Assignment_4_API_Testing_Muqadas_Shahid.pdf
│
├── Postman/
│   ├── Assignment_4_API_Testing_Postman_Collection.json
│   └── README.md
│
├── JMeter/
│   ├── Assignment_4_JMeter_Performance_Test.jmx
│   └── README.md
│
└── Screenshots/
    ├── Postman screenshots
    └── JMeter screenshots
