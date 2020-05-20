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

# Azure Stack expired certificates issue

## **Recommended Steps**

If you have validated the certificate, see [Using validated certificates](https://docs.microsoft.com/azure-stack/operator/azure-stack-validate-pki-certs#using-validated-certificates).

If you have not validated or obtain a new certificate, follow these steps:

1. [Prepare Azure Stack PKI certificate for use in deployment or rotation](https://docs.microsoft.com/azure-stack/operator/azure-stack-prepare-pki-certs)
2. You can use the Azure Stack Readiness Checker tool to validate the generated PKI certificate is suitable for pre-deployment: [Validate Azure Stack PKI certificates](https://docs.microsoft.com/azure-stack/operator/azure-stack-validate-pki-certs)
3. [Perform core services certificate validation](https://docs.microsoft.com/azure-stack/operator/azure-stack-validate-pki-certs#perform-core-services-certificate-validation)
4. [Perform platform as a service certificate validation](https://docs.microsoft.com/azure-stack/operator/azure-stack-validate-pki-certs#perform-platform-as-a-service-certificate-validation)

## **Recommended Documents**

- [Remediate common issues for Azure Stack PKI certificates](https://docs.microsoft.com/azure-stack/operator/azure-stack-remediate-certs)
- [Start-AzsReadinessChecker cmdlet reference](https://docs.microsoft.com/azure-stack/operator/azure-stack-azsreadiness-cmdlet)
- [Azure Stack certificates signing request generation](https://docs.microsoft.com/azure/azure-stack/azure-stack-get-pki-certs)
- [Azure Stack public key infrastructure certificate requirements](https://docs.microsoft.com/azure/azure-stack/azure-stack-pki-certs#certificate-requirements​)
- [ Prepare Azure Stack PKI certificates for use in deployment or rotation](https://docs.microsoft.com/azure-stack/operator/azure-stack-prepare-pki-certs)
- [Validate Azure Stack PKI certificates](https://docs.microsoft.com/azure/azure-stack/azure-stack-validate-pki-certs)
