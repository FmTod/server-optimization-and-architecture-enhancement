# Server Optimization and Architecture Enhancement

## This is our tech stack (The app is already containerized)
-  WebServer - Nginx
-  Language - PHP8
-  Caching - Redis (caching, session storage)
-  Search Index - Meilisearch
-  Database - MySQL
-  Monitoring - Prometheus/Grafana

## Cloud Service Selection:
1. Evaluate cloud service providers based on cost, expertise, and compatibility with the current architecture.
2. Assess the suitability of Linode Kubernetes for the expected architecture.
3. Research alternatives to managed database services like RDS for cost-effectiveness.

## Database Architecture:
1. Compare MySQL and MariaDB to determine the best engine for the specific use case.
2. Implement secure installation and configuration practices for the MySQL server.
3. Configure MySQL for optimal performance, including buffer pool size adjustment for faster query execution.
4. Integrate Prometheus MySQL exporter for monitoring server statistics.
5. Set up separate instances for reading and writing, starting with a main instance and a read replica.
6. Investigate and resolve the issue of MySQL connections remaining open.

## Database Optimization:
1. Analyze slow queries and propose schema, table, and engine level optimizations to enhance database performance.
2. Optimize storage engines based on the table structure and use cases.
3. Identify opportunities for optimizing columns and indexes based on the table structure and usage patterns.

## Infrastructure Optimization:
1. Ensure efficient utilization of the existing containerized application.
2. Design and implement a scalable and cost-effective infrastructure to support application services.
3. Conduct a cost analysis of different cloud service providers to determine the most suitable option.
4. Propose an infrastructure that enables independent scaling of application and database servers.
5. Deploy GitHub Actions on Kubernetes (K8s).
6. Note that Kubernetes implementation is pending and will be the responsibility of the DevOps team.
7. Cluster containers should include app pods (Laravel) as well as pods for Meilisearch, Soketi, and Redis.

## Infrastructure as Code (IAC) Implementation:
1. Utilize Terraform and Ansible to automate server infrastructure provisioning.
2. Develop IAC templates using Terraform for deploying the proposed server infrastructure.
3. Use Ansible or Terraform to provision servers, install specific packages, and set up server instances.

## Set up and configure web socket:
 1. Install and set up Soketi (www.docs.soketi.app) on the server.
 2. Configure Soketi to handle real-time communications.
 3. Test the functionality of Soketi to ensure it works as expected.
 4. Add the necessary code and configurations for Soketi or the chosen web socket server.
 5. Optimize web socket server for handling a large number of notifications

## Monitoring Tools Setup:
1. Configure a cost-effective separate instance for Prometheus and Grafana.
2. Deploy node exporter on all server instances for comprehensive monitoring.
3. Integrate MySQL exporter for monitoring the database instances.
4. Set up a Redis watcher to monitor the server running the Redis instance.
5. Enable notifications for monitoring alerts and events.

## Redis Instance Optimization:
1. Perform optimization techniques to enhance the performance of the Redis instance.

## Error Prevention and Smooth Transition Planning:
1. Develop strategies to prevent and mitigate errors, failures, and downtime.
2. Implement comprehensive testing procedures to ensure system stability and reliability.
3. Create a detailed plan for a smooth transition, considering potential errors, failures, and downtime scenarios.

## We need help with:
1. Which cloud service should we build the new architecture on? We are currently using Linode, which is cost-efficient, but the people we talk to do not have much experience with Linode. Our current expected architecture involves using the Linode Kubernetes.
2. Should we go with managed database services(like RDS, costly) or spin up our custom (cheap) orchestrated MySQL master/slave read replica setup.?
3. We are considering using the Kubernetes pods for services that we use, like Soketi, MeiliSearch, and Redis. Is that the right way, or should we just use the managed services?

### Please note that all the notes and questions above needs to be addressed in your architecture
### You can view related logs, sechma, curect stracture and documentaion here:
### https://drive.google.com/drive/u/3/folders/1LXSCfJAhO84jOhmwtB4zTOQpjrDErKhK
