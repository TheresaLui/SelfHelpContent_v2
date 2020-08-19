<properties
    pageTitle="Azure Stack Azure Active Directory"
    description="Azure Active Directory support in Azure Stack"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629193"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-security-aad"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Azure Active Directory

Azure Stack supports Azure Active Directory (Azure AD) in connected scenarios. Azure AD supports multiple tenants, and it can support multiple organizations, each in its own directory.

## **Recommended Steps**

1. Use the Azure Stack Readiness Checker tool to [validate that your Azure AD environment](https://docs.microsoft.com/azure/azure-stack/azure-stack-validate-identity) is ready to use with Azure Stack
2. If a validation check fails, details about the failure are output by the tool, including several common [validation failures](https://docs.microsoft.com/azure/azure-stack/azure-stack-validate-identity#validation-failures)
3. Once Azure AD integration is completed, you can use the portal to [Add a new Azure Stack tenant account](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-new-user-aad) in Azure Active Directory

## **Recommended Documents**

* [Overview of identity for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-identity-overview)
* [Identity architecture for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-identity-architecture)
* [Multi-tenancy in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-enable-multitenancy)