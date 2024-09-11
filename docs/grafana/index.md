# Grafana

## Overview
This section covers Grafana, an open-source platform for monitoring and observability.

## Contents
- [Introduction](grafana/introduction.md)
- [Dashboards](grafana/dashboards.md)
- [Data Sources](grafana/data_sources.md)

## Docker Setup
To test Grafana setups, you can use the following Docker setup.

### Dockerfile
Refer to the [Dockerfile](Dockerfile).

### How to Build and Run
1. Build the Docker image:
    ```bash
    docker build -t grafana .
    ```

2. Run the Docker container:
    ```bash
    docker run -it --rm grafana
    ```