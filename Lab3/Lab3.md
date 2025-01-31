# Lab3 Documentation

# On-Premises Solution Design

## Current on premises Architecture

The company is operating on in house components with following kind of key components.

1. Web Application
2. Databse
3. File Storage
4. Networking
5. Email Service

![Lab4](https://github.com/user-attachments/assets/4ad4a3fd-3c48-42fb-82cd-cfac8ff7468b)


# Section 2 Migration Strategy 

In order to enhance the scalability and reliability of the product the company considers to migrate the server to the cloud based solutions using Saas, Paas and Laas.

    Component                          Strategy                                                  Cloud Service Model

1. Web Application --> Deploy using cloud services like Virtual Machines and docker --> IaaS ( Virtual Machine ) and PaaS ( Kubernetes ).
2. SQL Database  --> Migrate to a managed database service such as AWS RDS, Azure SQL Database, or Google Cloud SQL --> PaaS Database management Service.
3. Local File Storafe --> Migrate to well managed database for example Azure SQL Database. --> PaaS ( Cloud Storage ).
4. Networking --> Move to cloud networking using virtual private cloud and managed services. --> SaaS ( Cloud Email API )


## Hybrid Approach Consideration
1. Before switching to a PaaS-managed database, the database can stay on IaaS for improved control.
2. Before moving the web application to a microservices-based PaaS solution, it can be lifted and moved to IaaS (VMs).

 ### Migration Plan Steps
Assessment & Planning
Conduct a dependency analysis to identify integrations between components.
Choose a cloud provider (AWS, Azure, GCP) based on cost, reliability, and compliance.
Database Migration

Backup and migrate the SQL database to an IaaS VM with SQL Server.
Optimize for PaaS transition (AWS RDS, Azure SQL, or GCP SQL).

Application Migration
Rehost monolithic web app on cloud-based VMs` (Lift and Shift).
Refactor into microservices using Kubernetes (PaaS).

Storage Migration
Transfer local files to AWS S3, Azure Blob, or Google Cloud Storage.
Configure lifecycle policies for cost efficiency.

Networking & Security
Set up Virtual Private Cloud  with security groups.
Implement Cloud-based Load Balancer & Firewalls**.

Email Services Migration
Transition from on-premises SMTP to SaaS-based solutions like AWS SES or SendGrid.
Integrate with the web application for seamless email notifications.

Testing & Optimizatio
Perform end-to-end testing of the new cloud environment.
Optimize costs and performance before full deployment.

 
