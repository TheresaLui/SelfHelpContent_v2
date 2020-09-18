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

# Azure Stack Preparing Certificates

## **Recommended Steps**

Once your certificates have been validated by the AzsReadinessChecker, you are ready to use them in your Azure Stack deployment or for Azure Stack secret rotation.

- For deployment, securely transfer your certificates to your deployment engineer, so that they can copy them onto the deployment host as specified in the [Azure Stack PKI requirements documentation](https://docs.microsoft.com/azure-stack/operator/azure-stack-pki-certs)
- For secret rotation, you can use the certificates to update old certificates for your Azure Stack environment's public infrastructure endpoints by following the [Azure Stack Secret Rotation documentation](https://docs.microsoft.com/azure-stack/operator/azure-stack-rotate-secrets)
- For PaaS services, you can use the certificates to install SQL, MySQL, and App Services Resource Providers in Azure Stack by following the [Overview of offering services in Azure Stack documentation](https://docs.microsoft.com/azure-stack/operator/azure-stack-offer-services-overview)

## **Recommended Documents**

- [Prepare Azure Stack PKI certificates for use in deployment and rotation](https://docs.microsoft.com/azure-stack/operator/azure-stack-prepare-pki-certs)
- [Remediate common issues for Azure Stack PKI certificates](https://docs.microsoft.com/azure-stack/operator/azure-stack-remediate-certs) 

