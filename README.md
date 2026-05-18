[README.md](https://github.com/user-attachments/files/27952786/README.md)
# Azure Infrastructure Deployment Templates

This repository contains Infrastructure as Code (IaC) templates and parameter files used for deploying Azure resources using **Bicep** and **ARM templates**.

## Repository Structure

```text
.
├── 03_azuredeploydisk.bicep
├── 04_az104-04-parameters
├── 04_az104-04-template
├── 06_az104-06-vms-parameters
├── 06_az104-06-vms-template
├── 07_az104-lab07-architecture-diagram
├── 10_az104-10-vms-edge-parameters
├── 10_az104-10-vms-edge-template
├── 11_az104-11-vm-template
```

---

## Contents

### 1. Disk Deployment
- **03_azuredeploydisk.bicep**
  - Bicep template for deploying and configuring Azure managed disks.

### 2. AZ-104 Lab 04 Templates
- **04_az104-04-template**
  - ARM/Bicep deployment template for Lab 04 resources.
- **04_az104-04-parameters**
  - Parameter file containing deployment-specific values.

### 3. AZ-104 Lab 06 Virtual Machines
- **06_az104-06-vms-template**
  - Template for deploying Azure Virtual Machines and related infrastructure.
- **06_az104-06-vms-parameters**
  - Parameters used for VM deployment.

### 4. Architecture Diagram
- **07_az104-lab07-architecture-diagram**
  - Visual architecture/reference diagram for Lab 07 deployment.

### 5. Edge VM Deployment
- **10_az104-10-vms-edge-template**
  - Template for deploying edge-related virtual machine infrastructure.
- **10_az104-10-vms-edge-parameters**
  - Deployment parameter values for edge VMs.

### 6. VM Deployment Template
- **11_az104-11-vm-template**
  - Generic Azure VM deployment template.

---

## Technologies Used

- Microsoft Azure
- ARM Templates
- Bicep
- Azure Virtual Machines
- Azure Managed Disks
- Infrastructure as Code (IaC)

---

## Prerequisites

Before deploying these templates, ensure you have:

- An active Azure subscription
- Azure CLI installed
- Required permissions on the target resource group/subscription

Install Azure CLI:

https://learn.microsoft.com/en-us/cli/azure/install-azure-cli

---

## Deployment Example

### Deploy using Azure CLI

```bash
az login

az deployment group create \
  --resource-group <RESOURCE_GROUP_NAME> \
  --template-file <TEMPLATE_FILE> \
  --parameters <PARAMETER_FILE>
```

Example:

```bash
az deployment group create \
  --resource-group myResourceGroup \
  --template-file 06_az104-06-vms-template.json \
  --parameters 06_az104-06-vms-parameters.json
```

---

## Learning Purpose

These templates were created as part of Azure Administrator (AZ-104) practice labs and infrastructure deployment exercises to gain hands-on experience with:
- Azure resource provisioning
- VM deployment and configuration
- ARM and Bicep templating
- Infrastructure automation

---

## Author

**Priyanshu Srivastava**

GitHub: https://github.com/

---

## License

This project is intended for educational and learning purposes.
