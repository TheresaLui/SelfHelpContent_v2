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
    cloudEnvironments="public"
    articleId="azurestack-name"
/>

# Azure Stack Secret Rotation

Only rotate secrets for Azure Stack Integrated Systems Version 1803 and later. Do not attempt secret rotation on pre-1802 Azure Stack versions.

Azure Stack uses various internal and external secrets to maintain secure communication between the Azure Stack infrastructure resources and services. Secrets include certificates, passwords, secure strings, and keys.

## **Recommended documents**

[Rotate secrets in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-rotate-secrets)