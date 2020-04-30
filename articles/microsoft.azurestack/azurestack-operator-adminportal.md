<properties
    pageTitle="Azure Stack Administration portal"
    description="Issues related to Azure Stack Admin Portal"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629245"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-operator-adminportal"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Administrator Portal

There are two portals in Azure Stack: the Administrator portal and the User portal (sometimes referred to as the tenant portal). Azure Stack operators use the Administrator portal for day-to-day management and operations of Azure Stack.

## **Recommended Steps**

To access the administrator portal, browse to the portal URL and sign in by using the credentials of an Azure Stack operator.

* For multi-node integrated systems, the portal address varies based on the region name and fully-qualified domain name (FQDN) of your Azure Stack deployment. It will match the pattern: `https://adminportal.<REGION>.<FQDN>`
* Verify [DNS name resolution](https://docs.microsoft.com/azure-stack/operator/azure-stack-integrate-dns) is working
* Access to the Administrator portal requires allowing traffic through TCP port 443. For more information, see [Azure Stack firewall integration](https://docs.microsoft.com/azure-stack/operator/azure-stack-firewall) and [Publish Azure Stack Services](https://docs.microsoft.com/azure-stack/operator/azure-stack-integrate-endpoints). 

## **Recommended Documents**

* [Using the administrator portal in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-portals)
