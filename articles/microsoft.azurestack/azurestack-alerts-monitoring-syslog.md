<properties
    pageTitle="Azure Stack Syslog Forwarding issues"
    description="Issues related to Azure Stack Syslog integration"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit, mquian, v-miegge"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629266"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="5b2386bf-2c63-409b-ba0e-a0cdcb23f2fa"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Syslog Forwarding Integration

Starting with the [1809 Update](https://docs.microsoft.com/azure/azure-stack/azure-stack-update-1809#new-features), Azure Stack has an integrated Syslog client that allows the forwarding of audits, alerts, and security logs related to the Azure Stack infrastructure to an external Syslog server or Security Information and Event Management (SIEM) system. Hardware partner-specific components can also be integrated with documentation from the hardware partner.

Starting with the [1904 Update](https://docs.microsoft.com/azure-stack/operator/azure-stack-release-notes-1904#fixes). Azure Stack fixed an issue where the syslog configuration was not persisted through an update cycle, causing the syslog client to lose its configuration, and the syslog messages to stop being forwarded. Syslog configuration is now preserved.

## **Recommended Steps**

1. [Integrate Azure Stack infrastructure with Syslog](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-security) with external security solutions already deployed in your datacenter
1. Configure [Syslog forwarding for network devices](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-physical-device-auditing#syslog-forwarding-for-network-devices) used by your Azure Stack environment
1. Check connectivity to syslog server and port
1. Follow OEM-specific documentation for integration Baseboard Management (BMC), Hardware Lifecycle Host (HLH), and other physical components with Syslog

## **Recommended Documents**

* [Integrate Azure Stack infrastructure with Syslog](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-security)<br>
* [Syslog forwarding for network devices](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-physical-device-auditing#syslog-forwarding-for-network-devices)
