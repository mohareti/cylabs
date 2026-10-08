# Monitoring Kubernetes with Prometheus and Grafana

##

Monitoring is a critical aspect of Kubernetes administration, providing insights into the health and performance of clusters and applications. Prometheus and Grafana are popular tools for monitoring Kubernetes environments. Prometheus collects and stores metrics as time series data, while Grafana is used for visualizing and querying the data collected by Prometheus.

### Setting up Prometheus and Grafana on Kubernetes

#### Prerequisites

* A running Kubernetes cluster.
* Helm installed: Helm is a package manager for Kubernetes, which simplifies deploying applications on Kubernetes.

#### Installation Using Helm Charts

1. **Add the Prometheus Helm Chart Repository**:

   ```bash
   helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
   helm repo update
   ```
2. **Install Prometheus**:
   * Install Prometheus using the Helm chart:

     ```bash
     helm install prometheus prometheus-community/prometheus
     ```
   * This command installs Prometheus with default settings. For custom configurations, you can create a `values.yaml` file and pass it with the installation command.
3. **Install Grafana**:
   * Add the Grafana Helm Chart Repository:

     ```bash
     helm repo add grafana https://grafana.github.io/helm-charts
     helm repo update
     ```
   * Install Grafana using Helm:

     ```bash
     helm install grafana grafana/grafana
     ```

#### Accessing Prometheus and Grafana

* After installation, both Prometheus and Grafana services are usually exposed as ClusterIP by default. To access them, you might need to change the service type to NodePort or LoadBalancer, or use port forwarding.
* For Grafana, you will need the admin password, which can be obtained by:

  ```bash
  kubectl get secret --namespace default grafana -o jsonpath="{.data.admin-password}" | base64 --decode ; echo
  ```

### Configuring Kubernetes Application Monitoring

1. **Configure Prometheus to Discover Targets**:
   * Prometheus discovers targets through Service Discovery. Ensure your application exposes metrics in a format that Prometheus can scrape.
   * Configure Prometheus by editing its config map to include the scrape configuration for your application.
2. **Visualize Metrics in Grafana**:
   * Access Grafana's dashboard, typically at `http://<NodeIP>:<NodePort>`.
   * Log in using the default username (`admin`) and the password obtained earlier.
   * Add Prometheus as a data source in Grafana by specifying the Prometheus service URL.
   * Import or create a dashboard in Grafana to visualize the metrics. You can use community dashboards or create custom ones according to your monitoring needs.

#### Sample Kubernetes Application Monitoring

* Let's say you have a Kubernetes application with Prometheus metrics exposed on `/metrics` endpoint.
* Update the Prometheus scrape config to include your application. This can be done by editing the `prometheus.yaml` in the Prometheus ConfigMap and adding your application under `scrape_configs`.
* Once Prometheus is configured and restarted, it should begin scraping metrics from your application.
* In Grafana, create a dashboard or import an existing one, and configure it to display the metrics collected from your application.

### Conclusion

Monitoring Kubernetes with Prometheus and Grafana provides deep insights into the performance and health of your clusters and applications. Using Helm to install these tools simplifies the process and allows for customizable configurations. Regularly monitoring your Kubernetes environment is key to maintaining a healthy and efficient system.
