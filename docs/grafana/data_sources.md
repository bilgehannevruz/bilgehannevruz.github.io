# Grafana Data Sources

## Overview
Data sources in Grafana are the databases or services from which Grafana retrieves data. Grafana supports a wide range of data sources, including time-series databases, SQL databases, and cloud services.

## Key Features
- **Wide Range of Integrations**: Supports popular data sources like Prometheus, InfluxDB, Elasticsearch, MySQL, PostgreSQL, and many more.
- **Custom Queries**: Allows you to write custom queries to retrieve specific data.
- **Authentication**: Supports various authentication methods to securely connect to data sources.
- **Plugins**: Extend Grafana's capabilities by adding new data source plugins.

## Example: Adding a Prometheus Data Source
Here is an example of how to add a Prometheus data source in Grafana.

### Steps
1. **Go to Configuration**:
    - Click on the gear icon in the sidebar to go to the Configuration page.
    - Select "Data Sources".

2. **Add Data Source**:
    - Click "Add data source".
    - Select "Prometheus" from the list of available data sources.

3. **Configure Data Source**:
    - Enter the URL of your Prometheus server (e.g., `http://localhost:9090`).
    - Configure any additional settings as needed.
    - Click "Save & Test" to verify the connection.

## Additional Resources
- [Grafana Data Sources Documentation](https://grafana.com/docs/grafana/latest/datasources/)
- [Grafana GitHub Repository](https://github.com/grafana/grafana)