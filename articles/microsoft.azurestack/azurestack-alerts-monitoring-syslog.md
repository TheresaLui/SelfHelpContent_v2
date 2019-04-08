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
	articleId="5b2386bf-2c63-409b-ba0e-a0cdcb23f2fa"
/>

# Azure Stack Syslog Forwarding Integration

Starting with the [1809 Update](https://docs.microsoft.com/azure/azure-stack/azure-stack-update-1809#new-features), Azure Stack has an integrated Syslog client that allows the forwarding of audits, alerts, and security logs related to the Azure Stack infrastructure to an external Syslog server or Security Information and Event Management (SIEM) system. Hardware partner-specific components can also be integrated with documentation from the hardware partner.

## **Recommended Steps**

1. [Integrate Azure Stack infrastructure with Syslog](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-security) with external security solutions already deployed in your datacenter<br>
2. Configure [Syslog forwarding for network devices](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-physical-device-auditing#syslog-forwarding-for-network-devices) used by your Azure Stack environment
3. Check connectivity to syslog server and port.
4. Follow OEM-specific documentation for integration Baseboard Management (BMC), Hardware Lifecycle Host (HLH), and other physical components with Syslog

## **Recommended Documents**

* [Integrate Azure Stack infrastructure with Syslog](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-security)<br>
* [Syslog forwarding for network devices](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-physical-device-auditing#syslog-forwarding-for-network-devices)
