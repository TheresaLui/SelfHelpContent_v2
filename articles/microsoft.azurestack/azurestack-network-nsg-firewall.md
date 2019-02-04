<properties
    pageTitle="Azure Stack firewall"
    description="Azure Stack firewall"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32567933"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-network-nsg-firewall"
/>

# Azure Stack firewall 
It's recommended that you use a firewall device to help secure Azure Stack. Although firewalls can help with things like distributed denial-of-service (DDOS) attacks, intrusion detection and content inspection, they can also become a throughput bottleneck for Azure storage services like blobs, tables, and queues.<br>

Based on the identity model Azure Active Directory (Azure AD) or Windows Server Active Directory Federation Services (AD FS), you might be required to publish the AD FS endpoint. If a disconnected deployment mode is used, you must publish the AD FS endpoint. For more information, see the [datacenter integration identity](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-identity) article.<br>

## **Recommended documents**

[Azure Stack firewall integration](https://docs.microsoft.com/azure/azure-stack/azure-stack-firewall)<br>

[Publish endpoints](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-endpoints)<br>

[Extension host](https://docs.microsoft.com/azure/azure-stack/azure-stack-extension-host-prepare)