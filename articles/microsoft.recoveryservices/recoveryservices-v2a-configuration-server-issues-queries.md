<properties
    pageTitle="VMware to Azure - Configuration server issues and queries"
    description="VMware to Azure - Configuration server issues and queries"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="asgang, v-miegge"
    ms.author="asgang"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32593224"
    resourceTags=""
    productPesIds="16370"
    cloudEnvironments="public"
    articleId="90810084-04fc-476b-9f39-445b2f3ce0a9"
/>

# VMware/Physical to Azure - Configuration server issues and queries

## Pre-requisites

1. Ensure that the [hardware requirements](https://docs.microsoft.com/azure/site-recovery/vmware-azure-deploy-configuration-server#prerequisites) to install a configuration server are met.
1. Ensure that all [necessary URLs are whitelisted](https://docs.microsoft.com/azure/site-recovery/vmware-azure-deploy-configuration-server#prerequisites) for successful configuration.
1. Set up the necessary [Azure Active Directory permissions](https://docs.microsoft.com/azure/site-recovery/vmware-azure-deploy-configuration-server#azure-active-directory-permission-requirements).

## Troubleshoot configuration server issues

* Failed to [register configuration server with virtual machine](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server#registration-failures)<br>
* Frequent shutdown or failed to [activate Windows license](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server#failure-to-activate-windows-license-from-server-standard-evaluation-to-server-standard)<br>
* [Configuration server disconnected/source machines greyed out](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server#remove-the-stale-entries-for-protected-items-from-the-configuration-server-database)<br>
* Configuration server [upgrade failure](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server#upgrade-fails-when-the-services-fail-to-stop)<br>
* [Azure active directory creation failure](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server#azure-active-directory-application-creation-failure)<br>
* Process server/Master target server [unable to communicate with configuration server](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-configuration-server#process-servermaster-target-are-unable-to-communicate-with-the-configuration-server)

## **Recommended Documents**

### Manage configuration server

* [Windows license update](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#update-windows-license)<br>
* How to [add a new vCenter server](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-vcenter#modify-the-vcenter-ip-address-and-port)<br>
* How to register [configuration server to a different vault](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#register-a-configuration-server-with-a-different-vault)<br>
* How to register [configuration server to the same vault](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#reregister-a-configuration-server-in-the-same-vault)<br>
* How to [delete/unregister configuration server](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#delete-or-unregister-a-configuration-server)<br>
* How to [generate configuration server passphrase](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#generate-configuration-server-passphrase)<br>
* How to [renew SSL certificates](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#renew-ssl-certificates)<br>
* How to [upgrade configuration server](https://docs.microsoft.com/azure/site-recovery/vmware-azure-manage-configuration-server#upgrade-the-configuration-server)
