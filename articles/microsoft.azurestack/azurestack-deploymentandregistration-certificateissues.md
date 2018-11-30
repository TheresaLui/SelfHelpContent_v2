<properties
    pageTitle="Title"
    description="Description"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    authorAlias="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629198, 32629199"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
/>

# Azure Stack Certificates Issues

During Azure Stack deployment, you will need to provide Secure Sockets Layer (SSL) certificates for public-facing endpoints. Details are outlined in the [Azure Stack public key infrastructure certificate requirements](https://docs.microsoft.com/azure/azure-stack/azure-stack-pki-certs) document.

**Note:** If your certificate issue is not related to initial deployment, please select the affected component instead.

## **Recommended steps**

* [Prepare Azure Stack PKI certificates for deployment](https://docs.microsoft.com/azure/azure-stack/azure-stack-prepare-pki-certs) from your CA of choice<br>
* [Prepare for extension host for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-extension-host-prepare) available starting with 1808 update and mandatory with 1811 update, which requires two additional certificates<br>
* [Validate Azure Stack PKI certificates](https://docs.microsoft.com/azure/azure-stack/azure-stack-validate-pki-certs) using the Azure Stack Readiness Checker tool<br>
* If necessary, [remediate common issues for Azure Stack PKI certificates](https://docs.microsoft.com/azure/azure-stack/azure-stack-remediate-certs)<br>
* Once certificates are successfully loaded, you can move on to [datacenter identity integration](https://docs.microsoft.com/azure/azure-stack/azure-stack-integrate-identity)<br>

## **Recommended documents**

* [Azure Stack Readiness Checker tool](https://aka.ms/AzsReadinessChecker)<br>