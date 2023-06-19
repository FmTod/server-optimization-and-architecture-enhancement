# Server Optimization and Architecture Enhancement

### This is our tech stack (The app is already containerized)
-  WebServer - Nginx
-  Language - PHP8
-  Caching - Redis (caching, session storage)
-  Search Index - Meilisearch
-  Database - MySQL
-  Monitoring - Prometheus/Grafana

## Requirements

### Cloud Service Selection:
1. Evaluate cloud service providers based on cost, expertise, and compatibility with the current architecture. <br>
<i>Linode is our preferred service provider due to its exceptional cost-effectiveness; nevertheless, we remain open to working with alternative providers if they offer similar or better features/services at a comparable cost</i>
2. Assess the suitability of Linode Kubernetes for the expected architecture.

### Database Architecture:
1. Compare MySQL and MariaDB to determine the best engine for the specific use case.
2. Implement secure installation and configuration practices for the MySQL server.
3. Configure MySQL for optimal performance, including buffer pool size adjustment for faster query execution.
4. Integrate Prometheus MySQL exporter for monitoring server statistics.
5. Set up separate instances for reading and writing, starting with a main instance and a read replica.
6. Investigate and resolve the issue of MySQL connections remaining open.

### Database Optimization:
1. Analyze slow queries and propose schema, table, and engine level optimizations to enhance database performance.
2. Optimize storage engines based on the table structure and use cases.
3. Identify opportunities for optimizing columns and indexes based on the table structure and usage patterns.

### Infrastructure Optimization:
1. Utilize Terraform and Ansible to automate server infrastructure provisioning (Kubernetes pods and database instances).
2. Ensure efficient utilization of the existing containerized application.
3. Design and implement a scalable and cost-effective infrastructure to support application services.
4. Propose an infrastructure that enables independent scaling of application and database servers.
5. Note that Kubernetes implementation is pending and will be the responsibility of the DevOps team.
6. Cluster containers should include app pods (Laravel) as well as pods for Meilisearch, Soketi, and Redis.
7. Pods should scale horizontally based on usage.
8. Optimize configurations of pods to fit the application needs and usage

### Error Prevention and Smooth Transition Planning:
1. Develop strategies to prevent and mitigate errors, failures, and downtime.
2. Implement comprehensive testing procedures to ensure system stability and reliability.
3. Create a detailed plan for a smooth transition, considering potential errors, failures, and downtime scenarios.

#### Please note that all the notes and questions above needs to be addressed in your architecture <br>You can view related logs, sechma, curect stracture and documentaion here: <br>https://drive.google.com/drive/u/3/folders/1LXSCfJAhO84jOhmwtB4zTOQpjrDErKhK
