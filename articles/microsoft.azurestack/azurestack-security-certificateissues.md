<properties
    pageTitle="Azure Stack Certificate Issues"
    description="Description"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629199"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="decac0d0-8da0-422f-a2b2-d3ad2f9ce05c"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Certificates Issues

During Azure Stack deployment, you will need to provide Secure Sockets Layer (SSL) certificates for public-facing endpoints. Details are outlined in the [Azure Stack public key infrastructure certificate requirements](https://docs.microsoft.com/azure/azure-stack/azure-stack-pki-certs) document.

**Note:** If your certificate issue is not related to initial deployment, please select the affected component instead.

## **Recommended Steps**

1. [Prepare Azure Stack PKI certificates for deployment](https://docs.microsoft.com/azure/azure-stack/azure-stack-prepare-pki-certs) from your CA of choice
2. [Prepare for extension host for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-extension-host-prepare), available starting with the 1808 update and mandatory with 1811 update, which requires two additional certificates
3. [Validate Azure Stack PKI certificates](https://docs.microsoft.com/azure/azure-stack/azure-stack-validate-pki-certs) using the Azure Stack Readiness Checker tool
4. If necessary, [remediate common issues for Azure Stack PKI certificates](https://docs.microsoft.com/azure/azure-stack/azure-stack-remediate-certs)
5. Once certificates are successfully loaded, you can move on to [datacenter identity integration](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-identity)

## **Recommended Documents**

* [Azure Stack Readiness Checker tool](https://aka.ms/AzsReadinessChecker)<br>
