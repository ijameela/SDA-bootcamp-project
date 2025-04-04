# Chatbot Project

## Project Stage 5: Moving to Azure VM Manually

### Stage Introduction

At this stage, we will move our application to an Azure VM. We’ll create a new VM and deploy our databases, frontend, and backend services on it. Additionally, we will manually set up the following components: an Azure network security group, an Azure Virtual Network, a public IP address, a subnet, a disk, and a network interface. Note that we will not use Infrastructure as Code (IaC) at this 
stage; everything will be set up manually.

![stage1-5](https://weclouddata.s3.us-east-1.amazonaws.com/cloud/project-stages/week3-stage5.png)

#### **VM Specifications:**

Operating System: `ubuntu-24_04-lts`
Instance Type: `Standard_D2ads_v6` or similar
Disk Size: `30GB`
Furthermore, systemd service files should be created for the databases, frontend, and backend services. These services should be enabled and started.

In the end, you should be able to access the application via the public IP address of the VM
