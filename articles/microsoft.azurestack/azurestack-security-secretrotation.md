<properties
    pageTitle="Azure Stack Secret Rotation Failure"
    description="Secret and certificate rotation in Azure Stack"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629257"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-security-secretrotation"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Secret Rotation

Azure Stack uses internal and external secrets to maintain secure communication between the Azure Stack infrastructure resources and services. Secrets include certificates, passwords, secure strings, and keys.

## **Recommended Steps**

1. When secrets are within 30 days of expiration, alerts are automatically generated in the Administrator Portal
2. Perform [prerequisites for secret rotation](https://docs.microsoft.com/azure/azure-stack/azure-stack-rotate-secrets#prerequisites) including preparing required certificates, checking stamp health, and notifying users of maintenance operations
3. Operators may notice alerts open and automatically close during rotation of Azure Stack secrets. This behavior is expected and the alerts can be ignored.
4. Complete the process of [rotating external secrets](https://docs.microsoft.com/azure/azure-stack/azure-stack-rotate-secrets#rotate-external-secrets) and [rotating internal secrets](https://docs.microsoft.com/azure/azure-stack/azure-stack-rotate-secrets#rotate-internal-secrets)
5. Follow separate steps to [update the baseboard management controller (BMC) credential](https://docs.microsoft.com/azure/azure-stack/azure-stack-rotate-secrets#update-the-bmc-credential)

## **Recommended Documents**

* [Rotate secrets in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-rotate-secrets)
* [Learn more about Azure Stack security](https://docs.microsoft.com/azure/azure-stack/azure-stack-security-foundations)
