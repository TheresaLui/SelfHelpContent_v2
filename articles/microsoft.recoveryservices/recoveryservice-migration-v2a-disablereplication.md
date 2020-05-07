<properties
    pageTitle="Disable replication in V2A"
    description="Disable replication in V2A"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="v-bllydi, TobyTu"
    ms.author="aaronmax"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32680605"
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="71842b51-f522-4acb-9ef4-f78c5e87ec25"
	ownershipId="Compute_SiteRecovery"
/>

# Disable replication in VMware to Azure

## **Recommended Steps**

### Protected servers

* [How to **disable replication and remove** a protected VM](https://docs.microsoft.com/azure/site-recovery/site-recovery-manage-registration-and-protection#disable-protection-for-a-vmware-vm-or-physical-server-vmware-to-azure)
* Use **Remove** to [disable replication if source environment is not accessible](https://docs.microsoft.com/azure/site-recovery/site-recovery-manage-registration-and-protection#disable-protection-for-a-vmware-vm-or-physical-server-vmware-to-azure)

### Configuration server

* [How to delete or unregister a configuration server](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#delete-or-unregister-a-configuration-server)
* [How to delete or unregister a configuration server by using PowerShell](https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-manage-configuration-server#delete-or-unregister-a-configuration-server-powershell)

### vCenter server

* [How to delete a vCenter server in Azure Site Recovery](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-vcenter#delete-a-vcenter-server)

## **Recommended Documents**

* [How to disable replication/ASR components and delete a Recovery Services vault](https://docs.microsoft.com/azure/site-recovery/delete-vault#delete-a-site-recovery-vault-1)
* [How to **force delete the vault by using powershell**](https://docs.microsoft.com/azure/site-recovery/delete-vault#use-powershell-to-force-delete-the-vault)
