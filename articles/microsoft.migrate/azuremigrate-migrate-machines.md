<properties
    pageTitle="Migrate machines"
    description="Troubleshoot issues in migration"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="anvar"
    ms.author="anvar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675755"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="e8de7410-ac8a-4fba-8e86-2c7c54838a8a"
    ownershipId="Compute_AzureMigrate"
/>

# Performing a migration on a replicating machine

## **Recommended Steps**

### **Migrate AWS VMs to Azure**

Follow the [guidance here.](https://go.microsoft.com/fwlink/?linkid=2137866)

### **Migrate physical servers/bare metal servers to Azure** 

Follow the [guidance here.](https://go.microsoft.com/fwlink/?linkid=2137867)

### **Migrate servers from other clouds (GCP, IBM Cloud, etc.) to Azure**

You can migrate most x64 servers by treating them as physical servers for the purpose of migration. Follow the [guidance here.](https://go.microsoft.com/fwlink/?linkid=2137963)

### **Migrate Azure VMs from one Azure region to another**

Use Azure Site Recovery (ASR) and follow the [guidance here.](https://go.microsoft.com/fwlink/?linkid=2137868)

### **I get an error that says that the core count limit was reached**

This happens when your subscription has run out of its allocated quota of virtual machine cores, and is unable to create the virtual machine. You can check the available quota by going to Subscription > Usage + quotas. You can have the quota increased by opening a support request to increase your virtual machine core count quota.

### **I get an error that says that the resource was disallowed by policy**

This happens when you have an Azure policy that enforces a naming convention on Azure resources that are created in the subscription. The migration operation creates Azure resources for the migrated virtual machine, it's disks and its network interface cards. Ensure that the policy doesn't disallow creation of virtual machines with the specified name. If you wish to change the name of the migrated virtual machine, you can do so before migration from the Compute and Network properties page for the replicating machine in the Server Migration tool.

### **I get an error that says 'VM Provisioning Failed', 'ComputeRpVmAllocationFailedV2', 'VMProvisioningTimeoutError', or 'FailedStartingVMError'**

As part of the  migration process, the Server Migration tool creates a temporary virtual machine in your Azure subscription. This temporary virtual machine is used to prepare the machines being migrated to make them operable in Azure. The preparation step includes things like enabling the essential Hyper-V drivers that are needed for proper functioning of the machine in Azure. This error indicates that creation of the temporary virtual machine failed. These kind of failures are mostly transient issues that go away on a retry. If you run into this issue, retry the operation again after 10 - 15 minutes.

### **I'm unable to connect to the migrated machine**

- Ensure that the on-premises machine was configured to allow remote connections to it
- For Linux machines, the on-premises (the actual machine being migrated) machine should have had SSH enabled and configured to start automatically on boot
- For Windows machines, the on-premises (the actual machine being migrated) machine should have had Remote Desktop enabled and remote desktop connections allowed by the Windows Firewall
- Ensure that there are no network security group rules that are blocking connections to the virtual machine in Azure
- [How to] [troubleshoot RDP connection to Windows VM?](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection)
- [How to] [troubleshoot SSH connection to Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/detailed-troubleshoot-ssh-connection)

### **The migrated machine doesn't have the Azure agent, and I am unable to install Azure VM extensions on the machine**

Server Migration installs the Azure agent on the virtual machine as part of the migration operation in certain scenarios as listed below. For other scenarios it is recommended that you install the Azure agent on the virtual machine post migration to Azure.

| Replication method  | For Windows machines  | For Linux machines |  
|---------|---------|---------|
|Agentless replication for VMware virtual machines     |  Requires manual installation post migration        | Requires manual installation post migration         |
|Agent-based replication for VMware virtual machines and physical servers     |   Installed by Server Migration tool</br>*(Not applicable for versions for which Azure VM agents aren't available)*      | Requires manual installation post migration      |
|Agentless replication of Hyper-V virtual machines     | Requires manual installation post migration        |   Requires manual installation post migration      |

### **I cannot see all VM SKUs while migrating to Azure Government**

The VM SKUs supported in the assessment and migration tools will depend on the availability in these Government regions. Comparison of Gov SKUs with respect to public cloud SKUs can be found [here](https://azure.microsoft.com/global-infrastructure/services/) by selecting region as Azure Government.

### **What are the target replication regions for migrating to Azure Government?**

Target regions for Azure Government are: US DoD Central, US DoD East, US Gov Arizona, US Gov Iowa, US Gov Texas, US Gov Virginia.
