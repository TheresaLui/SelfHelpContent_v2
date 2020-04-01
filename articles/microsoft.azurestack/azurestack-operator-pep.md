<properties
    pageTitle="Azure Stack Privileged Endpoint"
    description="Using the Azure Stack Privileged Endpoint(PEP)"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629247"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax"
    articleId="azurestack-operator-pep"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Using the Azure Stack Privileged Endpoint (PEP)

As an Azure Stack operator, you should use the administrator portal, PowerShell, or Azure Resource Manager APIs for most day-to-day management tasks. However, for some less common operations, you need to use the privileged endpoint (PEP).

## **Recommended Steps**

1. [Access the Privileged Endpoint (PEP)](https://docs.microsoft.com/azure/azure-stack/azure-stack-privileged-endpoint#access-the-privileged-endpoint) and [follow best practices](https://docs.microsoft.com/azure/azure-stack/azure-stack-privileged-endpoint#tips-for-using-the-privileged-endpoint) to perform low-level tasks, such as [collecting diagnostic logs](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostics#log-collection-tool)
2. Use the PEP to perform [post-deployment datacenter integration tasks](https://docs.microsoft.com/azure/azure-stack/azure-stack-customer-journey#post-deployment-phase), including:

    - [Adding Domain Name System (DNS) forwarders](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-dns#setting-up-conditional-forwarding-to-azure-stack)
    - [Integrating with your identity provider](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-identity)
    - [Perform certificate rotation](https://docs.microsoft.com/azure/azure-stack/azure-stack-rotate-secrets)

3. Always [close the privileged endpoint session](https://docs.microsoft.com/azure/azure-stack/azure-stack-privileged-endpoint#close-the-privileged-endpoint-session) when you are done using it

## **Recommended Documents**

- [Using the privileged endpoint in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-privileged-endpoint)
- [Azure Stack Log Collection Tool](https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostics#log-collection-tool)
