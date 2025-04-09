# Grafana Performance Testing Dashboards

This repository contains two pre-configured Grafana dashboards designed to visualize performance and load testing data stored in an InfluxDB database. These dashboards help analyze system behavior under load by providing insights into request and transaction metrics.

---

## Contents

- **Requests.json**: Dashboard focused on HTTP request-level metrics.
- **Transactions.json**: Dashboard focused on business transaction-level metrics.

---

## Prerequisites

- **Grafana** version 5.0.4 or higher
- **InfluxDB** as the data source for performance test data
- Performance/load testing tools that write metrics into InfluxDB (e.g., JMeter with InfluxDB backend listener)

---

## Dashboards Overview

### 1. Requests.json

This dashboard provides detailed insights into HTTP request performance, including:

- **Active Users**: Number of concurrent virtual users (threads)
- **Average Response Time**: Mean response time of requests over time
- **Request Count**: Total number of requests during the test
- **Error Rates**: (if available in data)
- **Time Series Graphs**: Visualize trends and spikes
- **Annotations**: Markers for test start and end events

### 2. Transactions.json

This dashboard focuses on business transactions, including:

- **Active Users**: Number of concurrent virtual users
- **Average Transaction Response Time**: Mean response time for transactions
- **Transaction Count**: Total number of transactions
- **Detailed Transaction Metrics**: Breakdown by transaction type
- **Annotations**: Markers for test start and end events

---

## How to Use

1. **Set up InfluxDB**  
   Ensure your performance testing tool is configured to write metrics into InfluxDB.

2. **Configure Grafana Data Source**  
   - Open Grafana
   - Navigate to **Configuration > Data Sources**
   - Add a new data source of type **InfluxDB**
   - Name it (e.g., `DS_HSLABOR`)  
   - Set the URL and database name matching your InfluxDB instance

3. **Import Dashboards**  
   - Go to **Create > Import** in Grafana
   - Upload `Requests.json` and `Transactions.json` files
   - When prompted, select your InfluxDB data source (e.g., `DS_HSLABOR`)
   - Click **Import**

4. **View Metrics**  
   Use the dashboards to monitor active users, response times, counts, and other key metrics during your performance tests.

---

## Customization

- **Variables**: Both dashboards support templating variables for flexible filtering.
- **Annotations**: Automatically highlight test start/end events.
- **Panels**: You can customize or add panels to suit your specific metrics.

---

## License

This repository is provided as-is for internal or educational use. Adapt and customize the dashboards as needed for your testing environment.

---

## Summary

These dashboards accelerate the analysis of performance test results by providing ready-made visualizations for HTTP requests and business transactions. Import them into Grafana, connect to your InfluxDB, and gain insights into your system's behavior under load.