<properties
    pageTitle="Azure Stack AD FS"
    description="AD FS integration in Azure Stack"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629187"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-security-adfs"
/>

# Azure Stack AD FS

Azure Stack supports AD FS in connected and disconnected scenarios. In disconnected mode, without a connection to the Internet, only AD FS is supported.

## **Recommended Steps**

1. Integrate Azure Stack with existing [Active Directory Federation Services and Graph](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-integrate-identity#active-directory-federation-services-and-graph)
2. [Add Azure Stack users in AD FS](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-users-adfs) for authentication with Azure Stack
3. If non-interactive logins are needed for a [common scenario that requires a service principal (SPN)](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-identity#spn-creation), follow steps to [Create service principal for AD FS](https://docs.microsoft.com/azure/azure-stack/azure-stack-create-service-principals)

## **Recommended Documents**

* [Add Azure Stack users in AD FS](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-users-adfs)
* [Overview of identity for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-identity-overview)
* [Identity architecture for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-identity-architecture)
* [Multi-tenancy in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-enable-multitenancy)