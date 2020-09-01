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
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-security-adfs"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack AD FS

Azure Stack supports Active Directory Federation Services (AD FS) in connected and disconnected scenarios. In disconnected mode, without a connection to the Internet, only AD FS is supported.

## **Recommended Steps**

1. Integrate Azure Stack with existing [Active Directory Federation Services and Graph](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-identity#active-directory-federation-services-and-graph)
2. [Add Azure Stack users in AD FS](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-users-adfs) for authentication with Azure Stack
3. If non-interactive logins are needed for a [common scenario that requires a service principal (SPN)](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-identity#spn-creation), follow steps to [Create service principal for AD FS](https://docs.microsoft.com/azure/azure-stack/azure-stack-create-service-principals)
4. The Azure Stack infrastructure must have network access to the Certificate Authority's Certificate Revocation List (CRL) location published in the certificate. This CRL must be an http endpoint. For more information, see [Azure Stack PKI certificate requirements](https://docs.microsoft.com/azure-stack/operator/azure-stack-pki-certs).  

## **Recommended Documents**

* [Add Azure Stack users in AD FS](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-users-adfs)
* [Overview of identity for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-identity-overview)
* [Identity architecture for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-identity-architecture)
* [Multi-tenancy in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-enable-multitenancy)
* [Validate AD FS](https://docs.microsoft.com/azure-stack/operator/azure-stack-validate-adfs)