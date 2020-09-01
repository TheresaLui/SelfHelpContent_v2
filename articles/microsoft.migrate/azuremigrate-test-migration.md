<properties
    pageTitle="Test migration"
    description="Troubleshoot issues in test migration"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="bsiva"
    ms.author="bsiva"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675759"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="8d7c9ca6-274a-4c0f-ac78-1aa9751d789c"
	ownershipId="Compute_AzureMigrate"
/>

# Performing a test migration

## **Recommended Steps**

### **I get an error that says that the core count limit was reached.**

This happens when your subscription has run out of its allocated quota of virtual machine cores, and is unable to create the test virtual machine. You can check the available quota by going to Subscription > Usage + quotas.

- Stop any running virtual machines in your Azure subscription that aren't being used to reclaim the quota used by it

- If you have sufficient quota to create a smaller sized virtual machine and don't need as many cores, you can update the target virtual machine size for the migration (and test migration). To update the target VM size for migration, click 'Replicating servers' on the Server Migration tool > click on the replicating machine to drill down to its overview page > Click 'Compute and Network' > update the target VM size, save and then retry test migration.

- You can have the quota increased by opening a support request to increase your virtual machine core count quota

### **I get an error that says that the resource was disallowed by policy.**

This happens when you have an Azure policy that enforces a naming convention on Azure resources that are created in the subscription. The test migration operation creates Azure resources for the test virtual machine, it's disks and its network interface cards. The resources created for the test migration have '-test' suffixed to its name. Ensure that the policy doesn't disallow this naming convention.

### **I get an error that says 'VM Provisioning Failed', 'ComputeRpVmAllocationFailedV2', 'VMProvisioningTimeoutError', or 'FailedStartingVMError'**

As part of the test migration process, the Server Migration tool creates a temporary virtual machine in your Azure subscription. This temporary virtual machine is used to prepare the machines being migrated to make them operable in Azure. The preparation step includes things like enabling the essential Hyper-V drivers that are needed for proper functioning of the machine in Azure. This error indicates that creation of the temporary virtual machine failed. These kind of failures are mostly transient issues that go away on a retry. If you run into this issue, retry the operation again after 10 - 15 minutes.

### **I'm unable to connect to the test virtual machine after performing a test migration.**

- Ensure that the on-premises machine allows remote connections

- For Linux machines, ensure that the on-premises (the actual machine being migrated) machine has SSH enabled and that it is configured to start automatically on boot

- For Windows machines, ensure that the on-premises (the actual machine being migrated) machine has Remote Desktop enabled and that remote desktop connections are allowed by the Windows Firewall

</br></br>If you need to fix a configuration on the on-premises machine, wait for a while to allow the configuration change to be replicated and then retry the test migration

- Ensure that there are no network security group rules that are blocking connections to the test virtual machine in Azure

- [How to] [troubleshoot RDP connection to Windows VM?](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection)

- [How to] [troubleshoot SSH connection to Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/detailed-troubleshoot-ssh-connection)