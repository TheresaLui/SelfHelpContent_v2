<properties
    pageTitle="VMware to Azure/Configuration server issues and queries"
    description="VMware to Azure/Configuration server issues and queries"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="anoopkv, asgang, v-miegge"
    ms.author="anoopkv"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32680603"
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="e454706c-0011-4f4c-bf93-be603d783a4c"
	ownershipId="Compute_SiteRecovery"
/>

# Configuration server issues and queries - VMware/Physical to Azure

## **Recommended Steps**

### VMware to Azure

**Prerequisites**

* Ensure the [hardware requirements](https://docs.microsoft.com/azure/site-recovery/vmware-azure-deploy-configuration-server#prerequisites) to install a configuration server are met
* Ensure that all [necessary URLs are whitelisted](https://docs.microsoft.com/azure/site-recovery/vmware-azure-deploy-configuration-server#prerequisites) for successful configuration
* Set up necessary [Azure Active Directory permissions](https://docs.microsoft.com/azure/site-recovery/vmware-azure-deploy-configuration-server#azure-active-directory-permission-requirements)

**Troubleshoot configuration server issues**

* Failed to [register configuration server with virtual machine](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server#registration-failures)
* Frequent shutdown or [failed to activate Windows license](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server#failure-to-activate-windows-license-from-server-standard-evaluation-to-server-standard)
* Configuration server [disconnected/source machines greyed out](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server#remove-the-stale-entries-for-protected-items-from-the-configuration-server-database)
* Configuration server [upgrade failure](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server#upgrade-fails-when-the-services-fail-to-stop)
* Azure active directory [creation failure](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server#azure-active-directory-application-creation-failure)
* Process server/Master target server [unable to communicate with configuration server](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server#process-servermaster-target-are-unable-to-communicate-with-the-configuration-server)

**Manage configuration server**

1. [Update the Windows license](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#update-windows-license)
1. [Add a new vCenter server](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-vcenter#modify-the-vcenter-ip-address-and-port)
1. [Generate configuration server passphrase](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#generate-configuration-server-passphrase)
1. [Renew SSL certificates](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#generate-configuration-server-passphrase)
1. [Upgrade configuration server](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#generate-configuration-server-passphrase)

**Delete/Re-register/Un-register configuration server**

1. Before deletion/un-registration, always [disable replication](https://docs.microsoft.com/azure/site-recovery/site-recovery-manage-registration-and-protection#disable-protection-for-a-vmware-vm-or-physical-server-vmware-to-azure)
1. Register configuration server to either the [same vault](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#reregister-a-configuration-server-in-the-same-vault), or to a [different vault]((https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#register-a-configuration-server-with-a-different-vault))
1. Delete/un-register configuration server through [portal](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#delete-or-unregister-a-configuration-server) or [PowerShell](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#delete-with-powershell)
1. Use Remove to [disable replication if source environment is not accessible](https://docs.microsoft.com/azure/site-recovery/site-recovery-manage-registration-and-protection#disable-protection-for-a-vmware-vm-or-physical-server-vmware-to-azure)

### Physical to Azure

1. Check [pre-requisites to install a Configuration Server using the Unified Setup](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#prerequisites)
1. Install new instance of Configuration Server [using the Unified Setup](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#download-the-latest-installation-file)
1. Change [proxy settings to connect the Configuration Server to the internet](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#modify-proxy-settings)
1. Re-register a Configuration Server (Physical) to either [the same vault](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#reregister-a-configuration-server-with-the-same-vault), or a [different vault](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#register-a-configuration-server-with-a-different-vault)
1. Troubleshoot [common installation and registration issues of Configuration Server](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#common-issues)
1. Delete or unregister a Configuration Server (Physical) - through [portal](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#common-issues) or [PowerShell](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#common-issues)
1. Re-register a Configuration Server (Physical) to either [the same vault](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#reregister-a-configuration-server-with-the-same-vault), or [a different vault](https://docs.microsoft.com/azure/site-recovery/physical-manage-configuration-server#register-a-configuration-server-with-a-different-vault)
