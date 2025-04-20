# Capstone Chatbot Project

## Project Stage 6: Postgres and Blob Storage on Azure with Terraform

### Stage Introduction

![stage1-6](https://weclouddata.s3.us-east-1.amazonaws.com/cloud/project-stages/week4-stage6.1.png)

Based on Stage 5, we are adding two new resources to the infrastructure: an Azure Database for PostgreSQL server and Azure Blob Storage. Instead of running PostgreSQL on the VM, we’ll use the Azure Database for PostgreSQL server for data storage, and files will be stored in Azure Blob Storage.

VM Specifications:

Operating System: ubuntu-24_04-lts
Instance Type: Standard_D2ads_v6 or similar
Disk Size: 30GB
PostgreSQL Database Specifications:

Public Access: Enabled
Workload Type: Development
Authentication Method: PostgreSQL authentication only
Firewall Rules: 0.0.0.0 - 255.255.255.255
A custom VM script should be created to:

Pull the latest code from the GitHub repository,
Install the required packages, and
Restart the frontend and backend services.
.env file in your VM
OPENAI_API_KEY=sk-...
DB_NAME=<azure postgres database name>
DB_USER=<azure postgres user name>
DB_PASSWORD=<azure postgres user password>
DB_HOST=<azure postgres server name>
DB_PORT=5432
AZURE_STORAGE_SAS_URL=...
AZURE_STORAGE_CONTAINER=...
CHROMADB_HOST=<public ip of the chromadb vm>
CHROMADB_PORT=8000
Additionally, systemd service files should be created for the frontend, and backend services. These services must be enabled and started.

GitHub Actions will be used as the CI/CD pipeline to trigger the VM custom script, ensuring that the VM automatically updates whenever a new commit is made.

In the end, you should be able to access the application via the VM’s public IP address, with data stored in the Azure Database for PostgreSQL server and files stored in Azure Blob Storage.
