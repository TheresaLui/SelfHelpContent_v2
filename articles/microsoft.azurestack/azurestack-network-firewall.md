<properties
    pageTitle="Azure Stack Network Infrastructure Firewall"
    description="Azure Stack Infrastructure Firewall"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629212"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-network-connectivity"
/>

# Azure Stack Infrastructure Network Connectivity

The Azure Stack solution requires a resilient and highly available physical infrastructure to support its operation and services.

It's recommended that you use a firewall device to help secure Azure Stack to provide intrusion detection, content inspection, and protection against denial-of-service (DoS) attacks.

Based on the identity model Azure Active Directory (Azure AD) or Windows Server Active Directory Federation Services (AD FS), you might be required to publish the AD FS endpoint. If a disconnected deployment mode is used, you must publish the AD FS endpoint. For more information, see the [datacenter integration identity](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-identity) article.

## **Recommended documents**

* [DNS integration](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-dns)
* [Firewall integration](https://docs.microsoft.com/azure/azure-stack/azure-stack-firewall)
* [Azure Stack Firewall Integration](https://docs.microsoft.com/azure/azure-stack/azure-stack-firewall)
* [Publish endpoints](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-endpoints)
* [Extension host](https://docs.microsoft.com/azure/azure-stack/azure-stack-extension-host-prepare)