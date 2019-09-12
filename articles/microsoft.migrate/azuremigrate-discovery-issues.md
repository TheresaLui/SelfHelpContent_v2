<properties
    pageTitle="Discovery issues"
    description="Discovery issues"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="An-mol"
    ms.author="anvar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675749"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public"
    articleId="3a672f3a-1f25-4ba7-92f8-cecd50db4097"
/>

# Discovery issues

## **Recommended Steps**

### **What data is collected by Azure Migrate: Server Assessment?**

The Azure Migrate appliance collects metadata about the on-premises VMs, the complete list of metadata collected by the appliance is listed in the following links:

[Metadata collected using Hyper-V appliance](https://aka.ms/migrate/hyperv/metadatacollected)

[Metadata collected using VMWare appliance](https://aka.ms/migrate/vmware/metadatacollected)

Additionally, if you are using the [dependency visualization functionality](https://aka.ms/migrate/agentbased/dependencies), the dependency agents collect details such as FQDN, OS, IP address, MAC address, processes running inside the VM and the incoming/outgoing TCP connections from the VM.

### **Machines are showing outdated information on the portal. How do I proceed?**

Ensure that the Azure Migrate appliance is up and running. Note that it takes 30 minutes for the latest information to reflect on the Azure Migrate portal. If you still see outdated information, you can perform a refresh using the steps listed [here.](https://aka.ms/migrate/discovery/refresh)

## Hyper-V VM discovery

### **I do not see the correct disk size on Hyper-V VMs. How do I proceed?**

This can happen if you have disks on SMB storage. In order to detect disk size correctly, it is required that CredSSP delegation is set up from the Azure Migrate appliance to the Hyper-V hosts discovered. [Learn more](https://aka.ms/migrate/diskdetails/credSSPdelegation) about how you can do this. 

### **I am facing WinRM errors while validating Hyper-V hosts. What should I do?**

Check whether Hyper-V hosts are ready for discovery by running this [script](https://aka.ms/migrate/hyperv/script) on the Hyper-V hosts.

### **How can I scope discovery for a multi-tenant environment in Azure Migrate?**

Hyper-V discovery is done using the Hyper-V host and cluster information provided. All VMs running on the hosts added to the Azure Migrate appliance are discovered. Scoping discovery to a single tenant that shares the hosts with other tenants is not supported today in Azure Migrate. 

### **How can I discover a large environment in Azure Migrate?**

Azure Migrate allows you to discover up to 10000 Hyper-V VMs in a single Azure Migrate project. A single appliance supports discovery of up to 5000 VMs. [Learn more](https://aka.ms/migrate/scale/hyperv) about how you can discover a large environment.

## VMWare VM discovery

### **How can I scope discovery for a multi-tenant environment in Azure Migrate?**

Azure Migrate allows you to split the discovery of your VMs to ensure that VMs of one tenant are not discovered in another tenant's subscription. [Learn more](https://aka.ms/migrate/vmware/multitenant) about how you can split the discovery in Azure Migrate.

### **How can I discover a large environment in Azure Migrate?**

Azure Migrate allows you to discover up to 35000 VMWare VMs in an Azure Migrate project. A single appliance can discover up to 10000 VMs. [Learn more]((https://aka.ms/migrate/vmware/multitenant)) about how you can discover a large environment.
