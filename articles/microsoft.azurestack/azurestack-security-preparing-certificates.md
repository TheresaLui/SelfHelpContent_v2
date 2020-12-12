<properties
    pageTitle="Azure Stack Preparing Certificates"
    description="Azure Stack Preparing Certificates"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="genlin"
    ms.author="mquian"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629198"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="5a850a45-94a3-4145-b2fc-6c4b3cdc4788"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Hub preparing certificates

Azure Stack Hub uses certificates for both external and internal secrets. The operator provides external certificates used during both initial deployment of Azure Stack Hub, and regular [secret rotation](https://docs.microsoft.com/azure-stack/operator/azure-stack-rotate-secrets).

 **This guidance pertains to certificates used for external secrets only**, as internal secret management does not require operator intervention. 

## **Recommended Steps**

1. First review [Azure Stack Hub public key infrastructure (PKI) certificate requirements](https://docs.microsoft.com/azure/azure-stack/azure-stack-pki-certs#certificate-requirements​).
2. Then [generate certificate signing requests](https://docs.microsoft.com/azure/azure-stack/azure-stack-get-pki-certs) for your certificates. 
3. [Prepare Azure Stack Hub PKI certificates for use in deployment or rotation](https://docs.microsoft.com/azure-stack/operator/azure-stack-prepare-pki-certs)
4. Then [validate Azure Stack Hub PKI certificates](https://docs.microsoft.com/azure-stack/operator/azure-stack-validate-pki-certs)

## **Recommended Documents**

[Fix common issues with Azure Stack Hub PKI certificates](https://docs.microsoft.com/azure-stack/operator/azure-stack-remediate-certs)

