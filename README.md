# Service Monitoring with Prometheus and Grafana
A project demonstrating how to set up a service monitoring system using Prometheus for metrics collection and Grafana for visualization. Includes step-by-step instructions for installation and configuration on AWS instances.

## Overview

This project demonstrates how to set up a service monitoring system using Prometheus and Grafana. Prometheus is used to collect and store metrics, while Grafana provides visualization and monitoring capabilities with a user-friendly interface.

## Installation

### 1. Create AWS Instances
   - Create a master instance and a node instance in AWS.

### 2. Install Prometheus on the Master Instance
   - SSH into the master instance.
   - Install Prometheus using your preferred package manager (e.g., apt or yum).
   - Configure Prometheus by editing the `prometheus.yml` configuration file located in the Prometheus installation directory (e.g., `/etc/prometheus/prometheus.yml`).
   - Add the targets (IP address and port number) of the node exporters on the node instance to the `scrape_configs` section of the `prometheus.yml` file.
   - Use port **9090** for accessing the Prometheus web interface.
   - Start Prometheus service and ensure it's running.

### 3. Install and Configure Node Exporter on the Node Instance
   - SSH into the node instance.
   - Download and install the Node Exporter binary.
   - Configure Node Exporter to expose metrics on port **9100**.
   - Start Node Exporter service and ensure it's running.

### 4. Install Grafana on the Master Instance
   - SSH into the master instance.
   - Download and install Grafana using your preferred method (e.g., package manager or binary).
   - Start Grafana service and ensure it's running. Access Grafana's web interface on port **3000**.

### 5. Configure Grafana to Connect to Prometheus
   - Open the Grafana web interface in your browser.
   - Log in using the default credentials (admin/admin).
   - Add Prometheus as a data source in Grafana, using the URL of your Prometheus server (http://<prometheus_ip>:9090).

### 6. Create Dashboards in Grafana
   - Create custom dashboards in Grafana to visualize metrics collected by Prometheus.
   - Add panels to the dashboards to display relevant metrics.
   - Customize the layout and appearance of the dashboards as needed.

## Additional Notes
- Ensure that security groups and firewall rules are properly configured to allow traffic between the master and node instances.
- Consider setting up alerts in Prometheus and Grafana to notify you of any abnormal conditions or threshold breaches.

## Conclusion
With Prometheus and Grafana set up and configured, you now have a powerful service monitoring system that provides insights into the performance and health of your infrastructure.
