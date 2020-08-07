<properties
    pageTitle="Test migration"
    description="Troubleshoot issues in test migration"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="anvar"
    ms.author="anvar"
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

This happens when your subscription has run out of its allocated quota of virtual machine cores and is unable to create the test virtual machine.

You can check the available quota by going to Subscription > Usage + quotas.

1. Get your quota increased by clicking on New Support Request > Select "Service and subscription limits (quota)" in "Issue type" > Select your subscription > Select an appropriate "Quote type"

Alternatively, you can do the following:

1. Stop any running virtual machines in your Azure subscription that aren't being used to reclaim the quota used by it
2. If you have sufficient quota to create a smaller sized virtual machine and don't need as many cores, you can update the target virtual machine size for the migration (and test migration):  Click 'Replicating servers' on the Server Migration tool > Click on the replicating machine > Click 'Compute and Network' > Update the ‘Target VM size’, save and then retry test migration.

### **I get an error that says that the resource was disallowed by policy.**

This happens when you have an Azure policy that enforces certain conventions. Few examples include:

1. A naming convention on Azure resources that are created in the subscription. The test migration operation creates Azure resources for the test virtual machine, its disks and its network interface cards. The resources created for the test migration have '-test' suffixed to its name. Ensure that the policy doesn't disallow this naming convention.
2. VM size that is not allowed. Ensure that policy doesn’t disallow the selected target VM size. You can update the target virtual machine size for the migration (and test migration): Click 'Replicating servers' on the Server Migration tool > Click on the replicating machine > Click 'Compute and Network' > Update the ‘Target VM size’, save and then retry test migration.
3. Policy requires resources to be created with certain Resource Tags. This is currently not supported by Server Migration tool. Tagging can be done post migration. You can create a policy exception for the duration of migration to allow migration to succeed.

### **I'm unable to connect to the test virtual machine after performing a test migration.**

- Ensure that the on-premises machine allows remote connections
- For Linux machines, ensure that the on-premises (the actual machine being migrated) machine has SSH enabled and that it is configured to start automatically on boot
- For Windows machines, ensure that the on-premises (the actual machine being migrated) machine has Remote Desktop enabled and that remote desktop connections are allowed by the Windows Firewall

If you need to fix a configuration on the on-premises machine, wait for a while to allow the configuration change to be replicated and then retry the test migration. Ensure that there are no network security group rules that are blocking connections to the test virtual machine in Azure.

## **Recommended Documents**

- [How to] [troubleshoot RDP connection to Windows VM?](https://docs.microsoft.com/azure/virtual-machines/windows/troubleshoot-rdp-connection)
- [How to] [troubleshoot SSH connection to Linux VM](https://docs.microsoft.com/azure/virtual-machines/linux/detailed-troubleshoot-ssh-connection)
