<properties
    pageTitle="I am unable to install the mobility service agent due to connectivity issues"
    description="Questions or issues related to connectivity failures like URL whitelist or express route"
    service="microsoft.recoveryservices"
    resource="vaults"
    authors="v-miegge"
    ms.author="sideeksh"
    selfHelpType="generic"
    supportTopicIds="32744985"
    resourceTags=""
    productPesIds="16370"
    ownershipId="Compute_SiteRecovery"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="6ce2c7cc-7f07-4913-839f-bca3fde8bbe6"
/>

# I am unable to install the mobility service agent due to connectivity issues

Mobility agent installation failed due to connectivity failures? Follow the below troubleshooting guidance to resolve most commonly seen errors:

## **Recommended Steps**

### Azure to Azure DR

- Resolve connectivity errors with [ids: 151037, 151072, 151195, 151196)](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-network-connectivity)
- Set up the NSG to whitelist specific URLs for [communication with Azure services](https://docs.microsoft.com/azure/site-recovery/azure-to-azure-troubleshoot-network-connectivity#example-nsg-configuration)

### VMware to Azure DR

- Ensure that all network requirements are met on configuration server to allow [communication with Azure services](https://docs.microsoft.com/azure/site-recovery/vmware-azure-deploy-configuration-server#network-requirements)
- Resolve connectivity errors with [ids: 95117, 95118, 95523, 95105, 95106](https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install#connectivity-failure-errorid-95117--97118)
- Ensure that the necessary folders are excluded from anti-virus to avoid [communication blockers](https://docs.microsoft.com/azure/site-recovery/vmware-azure-set-up-source#azure-site-recovery-folder-exclusions-from-antivirus-program)
- Ensure that the process server is connected and the source machine is able to [communicate with process server](https://docs.microsoft.com/azure/site-recovery/vmware-physical-azure-troubleshoot-process-server#check-connectivity-and-replication)
