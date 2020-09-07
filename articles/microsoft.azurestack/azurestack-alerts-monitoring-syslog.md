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

# Azure Stack Hub Syslog Forwarding Integration

**NOTE**: Before you create a support ticket, review [**Release notes**](https://docs.microsoft.com/azure-stack/operator/release-notes) and [**Known issues**](https://docs.microsoft.com/azure-stack/operator/known-issues) for the update you are applying (choose from the Version drop-down menu). This may save you time and effort.

## **Recommended Steps**

1. [Integrate Azure Stack Hub infrastructure with Syslog](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-security) with external security solutions already deployed in your datacenter
1. Configure [Syslog forwarding for network devices](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-physical-device-auditing#syslog-forwarding-for-network-devices) used by your Azure Stack Hub environment
1. Check connectivity to Syslog server and port
1. Follow OEM-specific documentation for integration Baseboard Management (BMC), Hardware Lifecycle Host (HLH), and other physical components with Syslog

## **Recommended Documents**

* [Integrate Azure Stack Hub infrastructure with Syslog](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-security)<br>
* [Syslog forwarding for network devices](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-physical-device-auditing#syslog-forwarding-for-network-devices)
