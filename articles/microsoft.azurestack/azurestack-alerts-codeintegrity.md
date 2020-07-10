<properties
    pageTitle="Azure Stack Code Integrity"
    description="General guidance for Azure Stack code integrity"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629201"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-alerts-codeintegrity"
    ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Code Integrity

Azure Stack Hub makes use of the latest Windows Server security features. One of them is [Windows Defender Application Control](https://docs.microsoft.com/windows/security/threat-protection/device-guard/introduction-to-device-guard-virtualization-based-security-and-windows-defender-application-control) (WDAC, formerly known as Code Integrity), which provides executables whitelisting and ensures that only authorized code runs within the Azure Stack Hub infrastructure.

Azure Stack Hub enforces both User Mode Code Integrity (UMCI) and Hypervisor Code Integrity (HVCI). Only software that has been approved to run in the Azure Stack Hub infrastructure can be executed. Any attempt to execute unauthorized code is blocked and an alert is generated. Support assistance is required to resolve this alert.

## **Recommended Documents**

* [Azure Stack infrastructure security posture - Code Integrity](https://docs.microsoft.com/azure-stack/operator/azure-stack-security-foundations#windows-defender-application-control)