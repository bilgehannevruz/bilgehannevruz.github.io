# Azure (Microsoft Azure)

## Overview
Microsoft Azure is a cloud computing service created by Microsoft for building, testing, deploying, and managing applications and services through Microsoft-managed data centers. It provides a range of cloud services, including those for compute, analytics, storage, and networking.

## Key Services
- **Azure Virtual Machines**: Provides on-demand, scalable computing resources.
- **Azure Blob Storage**: Massively scalable object storage for unstructured data.
- **Azure SQL Database**: Fully managed relational database with built-in intelligence.

## Example: Creating a Virtual Machine
Here is an example of how to create a virtual machine using the Azure CLI.

### Prerequisites
- Azure CLI installed and configured with your credentials.

### Commands
1. Create a resource group:
    ```sh
    az group create --name MyResourceGroup --location eastus
    ```

2. Create a virtual machine:
    ```sh
    az vm create \
      --resource-group MyResourceGroup \
      --name MyVM \
      --image UbuntuLTS \
      --admin-username azureuser \
      --generate-ssh-keys
    ```

3. Get the public IP address of the virtual machine:
    ```sh
    az vm list-ip-addresses --resource-group MyResourceGroup --name MyVM --output table
    ```

## Additional Resources
- [Azure Virtual Machines Documentation](https://docs.microsoft.com/en-us/azure/virtual-machines/)
- [Azure Blob Storage Documentation](https://docs.microsoft.com/en-us/azure/storage/blobs/)
- [Azure SQL Database Documentation](https://docs.microsoft.com/en-us/azure/sql-database/)