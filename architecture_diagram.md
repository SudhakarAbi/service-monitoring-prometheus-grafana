### Architecture Diagram

This architecture diagram illustrates how Prometheus and Grafana can be used together for monitoring applications and infrastructure. 
Prometheus collects metrics data from application endpoints, which can then be visualized and analyzed using Grafana. 
The Alertmanager component allows users to define alerting rules and receive notifications for critical events.
          
            +---------------------+
            |    Grafana Server   |
            |       (3000)        |
            +----------+----------+
                       |
                       | Grafana provides a user-friendly interface for visualization and monitoring.
                       | Users can create custom dashboards to visualize metrics collected by Prometheus.
                       |
            +----------+----------+
            |     Prometheus      |
            |   (Data Collector)   |
            |       (9090)         |
            +----------+----------+
                       |
                       | Prometheus is responsible for collecting, storing, and querying metrics data.
                       | It scrapes metrics from application endpoints and stores them in a time-series database.
                       |
            +----------+----------+
            |     Node Exporter   |
            |    (On Each Node)   |
            |       (9100)         |
            +---------------------+
                       |
                       | Application Endpoints: These are endpoints within your applications that expose metrics.
                       | Prometheus scrapes these endpoints to collect metrics data.


You can customize this diagram further based on your specific setup and requirements. 
For example, you could include additional components such as exporters for collecting metrics from specific services or databases.
