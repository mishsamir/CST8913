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
1. To migrate SQL Server to Azure SQL Database, use the Azure Database Migration Service.
2. In the application settings, change the connection string.
3. Improve performance tuning and indexes.

### Step 3: Convert Background Jobs into Azure Functions

1. Determine the background operations.
2. Turn them into Azure Functions that are activated by:
3. Queue Storage (processing messages).
4. Use the Azure Functions App to deploy functions.

### Step 4: Store Static Content and Logs in Azure Blob Storage
1. Transfer the virtual machine's logs, pictures, and other static assets to Azure Blob Storage.
2. To retrieve assets from the Blob Storage URL, update the application.
3. Make use of the REST API or Azure Storage SDK in the application.

### Step 5: Setting up Azure AD 

1. Set up OAuth 2.0 authentication and register the application in Azure AD.
2. Make the web application compatible with Azure AD authentication.
3. Use Azure AD roles and JWT tokens to secure APIs.

### Step 6: Monitoring & Logging (Azure Monitor)
1. To enable real-time telemetry, enable Application Insights in Azure App Service.
2. Set up Log Analytics to gather logs from applications.
3. Configure notifications for malfunctions and performance problems.
