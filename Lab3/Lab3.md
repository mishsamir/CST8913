# Lab3 Documentation

# On-Premises Solution Design

## Current on premises Architecture

The company is operating on in house components with following kind of key components.

1. Web Application
2. Databse
3. File Storage
4. Networking
5. Email Service

![Lab3 Architecture](https://github.com/user-attachments/assets/aece4fb4-5ffa-4849-8987-17ef1bf3e1c1)

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

 ### **Migration Plan Steps**

#### **1. Assessment & Planning**
- Conduct a **dependency analysis** to identify integrations between components.
- Choose a **cloud provider** (AWS, Azure, GCP) based on cost, reliability, and compliance.

#### **2. Database Migration**
- Backup and migrate the SQL database to an **IaaS VM** with SQL Server.
- Optimize for **PaaS transition** (AWS RDS, Azure SQL, or GCP SQL).

#### **3. Application Migration**
- Rehost monolithic web app on **cloud-based VMs** (Lift and Shift).
- Refactor into **microservices** using **Kubernetes** (PaaS).

#### **4. Storage Migration**
- Transfer local files to **AWS S3, Azure Blob, or Google Cloud Storage**.
- Configure lifecycle policies for **cost efficiency**.

#### **5. Networking & Security**
- Set up **Virtual Private Cloud (VPC)** with security groups.
- Implement **Cloud-based Load Balancer & Firewalls**.

#### **6. Email Services Migration**
- Transition from on-premises SMTP to **SaaS-based solutions** like AWS SES or SendGrid.
- Integrate with the web application for seamless email notifications.

#### **7. Testing & Optimization**
- Perform end-to-end testing of the new cloud environment.
- Optimize costs and performance before full deployment.

 
