<properties
    pageTitle="Azure Stack expired certificates issue"
    description="Azure Stack expired certificates issue"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="genlin"
    ms.author="mquian"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32663931"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="60efa9c9-73df-4816-9eab-40409496cc66"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Hub expired certificates issue

Azure Stack Hub uses certificates for both external and internal secrets. When certificates are within 30 days of expiration, the following alerts are generated in the administrator portal:

- Pending internal certificate expiration
- Pending external certificate expiration

External secrets are used to secure endpoints on external infrastructure and services, and are provided by the Azure Stack Hub operator. Internal secrets are used by the Azure Stack Hub infrastructure without intervention of the Azure Stack Hub Operator.

In order to resolve alerts for expired certificates, you need to rotate new certificates in their place. The process for rotating expired certificates is different for external and internal certificates.

## **Recommended Steps**

When certificates are about to expire or have expired, they are updated through the [certificate rotation process](https://docs.microsoft.com/azure-stack/operator/azure-stack-rotate-secrets). This article outlines the prerequisite steps you need to take, and provides details on how to rotate the certificates used for both external and internal secrets. The article also provides details on where to get help for rotating external certificates used by value-add resource providers.

## **Recommended Documents**

[Rotate secrets in Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-rotate-secrets)

The following recommended documents pertain only to certificates used for external secrets, provided by the Azure Stack Hub operator:

- [Azure Stack Hub public key infrastructure (PKI) certificate requirements](https://docs.microsoft.com/azure/azure-stack/azure-stack-pki-certs#certificate-requirements​)
- [Generate certificate signing requests for Azure Stack Hub](https://docs.microsoft.com/azure/azure-stack/azure-stack-get-pki-certs)
- [Prepare Azure Stack PKI certificates for use in deployment or rotation](https://docs.microsoft.com/azure-stack/operator/azure-stack-prepare-pki-certs)
- [Validate Azure Stack Hub PKI certificates](https://docs.microsoft.com/azure-stack/operator/azure-stack-validate-pki-certs)
- [Fix common issues with Azure Stack Hub PKI certificates](https://docs.microsoft.com/azure-stack/operator/azure-stack-remediate-certs)
