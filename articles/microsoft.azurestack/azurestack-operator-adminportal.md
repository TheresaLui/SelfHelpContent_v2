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

To access the administrator portal, you only need to go the portal URL and sign in as an Azure Stack operator. Most support questions related to the Administrator portal are covered in the following steps. 


## **Recommended Steps**

* For multi-node integrated systems, the portal address varies based on the region name and fully-qualified domain name (FQDN) of your Azure Stack deployment. It will match the pattern: `https://adminportal.<REGION>.<FQDN>`
* Verify [DNS name resolution](https://docs.microsoft.com/azure-stack/operator/azure-stack-integrate-dns) is working
* Access to the Administrator portal requires allowing traffic through TCP port 443. For more information, see [Azure Stack firewall integration](https://docs.microsoft.com/azure-stack/operator/azure-stack-firewall) and [Publish Azure Stack Services](https://docs.microsoft.com/azure-stack/operator/azure-stack-integrate-endpoints) 
* If the portal is unavailable, and no type of patch, update, or field replacement is in progress, you can run the following command to remediate the problem:

  ```
  Test-AzureStack -Repair -Include AzsPortalAPISummary
  ```



## **Recommended Documents**

* [Using the administrator portal in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-portals)
