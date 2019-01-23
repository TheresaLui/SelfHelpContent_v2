<properties
    pageTitle="Azure Stack Syslog Forwarding issues"
    description="Issues related to Azure Stack Syslog integration"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629266"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
/>

# Azure Stack Syslog Forwarding Integration

Starting with the [1809 update](https://docs.microsoft.com/azure/azure-stack/azure-stack-update-1809#new-features), Azure Stack has an integrated Syslog client. This client allows the forwarding of audits, alerts, and security logs related to the Azure Stack infrastructure to a syslog server or security information and event management (SIEM) software external to Azure Stack. Hardware-partner specific components can be integrated with documentation from the hardware partner.

## **Recommended steps**

1. [Integrate Azure Stack infrastructure with Syslog](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-security) with external security solution(s) already deployed in your datacenter
2. Configure [Syslog forwarding for network devices](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-physical-device-auditing#syslog-forwarding-for-network-devices) used by your Azure Stack environment
3. Follow OEM-specific documentation for integration Baseboard MAnagement (BMC), Hardware Lifecycle Host (HLH) and other physical components with Syslog

## **Recommended documents**

* [Integrate Azure Stack infrastructure with Syslog](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-security)<br>
* [Syslog forwarding for network devices](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-physical-device-auditing#syslog-forwarding-for-network-devices)