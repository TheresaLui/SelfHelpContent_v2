<properties
    pageTitle="Azure Stack Network Connectivity"
    description="Azure Stack Infrastructure Network Connectivity"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629178,32629204"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-network-connectivity"
/>

# Azure Stack Infrastructure Network Connectivity

The Azure Stack solution requires a resilient and highly available physical infrastructure to support its operation and services.

Use these recommended documents to help you decide how to best integrate Azure Stack into your existing networking environment.

It's recommended that you use a firewall device to help secure Azure Stack. Although firewalls can help with things like distributed denial-of-service (DDOS) attacks, intrusion detection and content inspection, they can also become a throughput bottleneck for Azure storage services like blobs, tables, and queues.

Based on the identity model Azure Active Directory (Azure AD) or Windows Server Active Directory Federation Services (AD FS), you might be required to publish the AD FS endpoint. If a disconnected deployment mode is used, you must publish the AD FS endpoint. For more information, see the [datacenter integration identity](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-identity) article.

## **Recommended documents**

* [Network integration](https://docs.microsoft.com/azure/azure-stack/azure-stack-network)
* [Border connectivity](https://docs.microsoft.com/azure/azure-stack/azure-stack-border-connectivity)
* [DNS integration](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-dns)

* [Firewall integration](https://docs.microsoft.com/azure/azure-stack/azure-stack-firewall)
* [Azure Stack firewall integration](https://docs.microsoft.com/azure/azure-stack/azure-stack-firewall)
* [Publish endpoints](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-endpoints)
* [Extension host](https://docs.microsoft.com/azure/azure-stack/azure-stack-extension-host-prepare)