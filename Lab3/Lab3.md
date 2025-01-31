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
