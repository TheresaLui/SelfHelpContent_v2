<properties
    pageTitle="Azure Stack Readiness Checker"
    description="Azure Stack Readiness Checker"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629251"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-deployment-readiness"
/>

# Azure Stack Readiness Checker

You can the use Azure Stack Readiness Checker tool to validate Azure Stack PKI certificates prior to deployment. The tool checks to ensure that certificates meet the [PKI requirements](https://docs.microsoft.com/azure/azure-stack/azure-stack-pki-certs) of an Azure Stack deployment and Azure Stack Secret Rotation, and logs the results in a report file.

## **Recommended steps**

1. Get the Azure Stack Readiness Checker tool [from the PowerShell Gallery](https://aka.ms/AzsReadinessChecker)
2. [Perform core services certificate validation](https://docs.microsoft.com/azure/azure-stack/azure-stack-validate-pki-certs#perform-core-services-certificate-validation) to prepare and validate the Azure Stack PKI certificates for deployment and [secret rotation](https://docs.microsoft.com/azure/azure-stack/azure-stack-rotate-secrets)
3. If SQL/MySQL or AppService deployments are planned, [Perform platform as a service (PaaS) certificate validation
](https://docs.microsoft.com/azure/azure-stack/azure-stack-validate-pki-certs#perform-platform-as-a-service-certificate-validation) to prepare the certificates for platform-as-a-service (PaaS) applications

## **Recommended documents**

[Azure Stack public key infrastructure certificate requirements](https://docs.microsoft.com/azure/azure-stack/azure-stack-pki-certs)<br>
[Azure Stack Readiness Checker tool ](https://aka.ms/AzsReadinessChecker)