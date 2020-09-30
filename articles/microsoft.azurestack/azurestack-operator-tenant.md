<properties
    pageTitle="Azure Stack Tenant Management"
    description="Issues related to Azure Stack tenant management"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629269"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-operator-tenant"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Tenant Management

There are two portals in Azure Stack: the administration portal and the user portal (sometimes referred to as the tenant portal). You can use the Azure Stack user portal to subscribe to public offers and use the services that these offers provide. If you've used the global Azure portal, you're already familiar with how the user portal works.

## **Recommended Steps**

Your Azure Stack operator (either a service provider or an administrator in your organization) will let you know the correct URL to access the portal.

* To register your Azure Stack environment, [Connect to Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-version-profiles-azurecli2#connect-to-azure-stack), using the right parameters for your environment
* For multi-node integrated systems, the address will match the pattern `https://portal.&lt;*region*&gt;.&lt;*FQDN*&gt;`

## **Recommended Documents**

- [Use the Azure Stack portal](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-use-portal)
- [Add a new Azure Stack tenant account in Azure Active Directory](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-new-user-aad)
