# Refactoring a Legacy Application for Cloud-Native Deployment on Azure
## Task 1: Monolithic Architecture Components and Dependencies
1. Windows Server 2019 virtual machine (Azure VM) contains a monolithic web application. The application contains the frontend, which was developed using React.js, and the backend service, which is used with Node.js and the SQL server database.
2. Dependencies: Frontend directly calls backend APIs, which interact with the SQL Server database which is in the same VM.
2. Public load balancer is used to distribute the incoming traffic across the VMs, which have the same configurations. A public load balancer maps the public IP and port of incoming traffic to the private IP and port of the VM.
### Monolithic architecture Diagram.
![assignment](https://github.com/user-attachments/assets/5cdf5003-d3cb-418c-a080-a6dc27b7eabd)

## Task 2: Refactoring Strategy
### Break down the monolithic application into microservices
1. Azure Static Web Apps hosts static webpages.
2. Node.js-written backend services, such as product-service and order-service, are integrated into Azure web apps, where the runtime stack is available as a node programming language.
3. The Azure SQL database hosts the virtual machine-hosted SQL server.
4. Azure functions are used to implement the message queue system.
5.  Across several Azure and non-Azure subscriptions and tenants, Azure Monitor gathers and combines data from each tier and component of your system.

## Task 3: Implement Refactoring Changes
### Step 1: Deploy the Frontend to Azure App Service

1. Package the web application frontend (React) and push the code to the GitHub repository.
2. Build a static web application in Azure.
3. Use the Azure web application with the runtime stack as the node programming language for the backend service.  The services can be deployed straight from the GitHub actions.
4. Use GitHub Actions to deploy the backend and frontend code.

### Step 2: Migrate the Database to Azure SQL Database
