<properties
    pageTitle="Azure Stack Hub DNS Integration"
    description="Azure Stack Hub infrastructure integration with customer DNS"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629209"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-netinfra-dns"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Hub Infrastructure DNS Integration

## **Recommended Steps**

If you are integrating Azure Stack Hub with your corporate DNS, see [DNS integration](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-dns).

If you need to change the DNS forwarders that Azure Stack Hub was deployed with, connect to the privileged endpoint and run `Get-AzSDnsForwarder` and `Set-AzSDnsForwarder`. For more information, see [Use the privileged endpoint in Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-privileged-endpoint).

## **Recommended Documents**

* [Setting up conditional forwarding to Azure Stack Hub](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-dns#setting-up-conditional-forwarding-to-azure-stack)
* [Delegating the external DNS zone to Azure Stack Hub](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-dns#delegating-the-external-dns-zone-to-azure-stack)
