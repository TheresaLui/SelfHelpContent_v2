<properties
    pageTitle="Renew expired certificate"
    description="Renew expired certificate"
    service="microsoft.network"
    resource="applicationgateways"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder="36"
    selfHelpType="resource"
    articleId="7640a487-6f9f-4a3c-9e53-5c75862cc1f6"
    resourceTags=""
    productPesIds="15922"
    supportTopicIds="32783366"
    cloudEnvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
    ownershipId="CloudNet_AzureApplicationGateway"
/>

# Renew expired certificate

## **Recommended Steps**

You can renew SSL certificates in Application Gateway using the **renew** option in the Azure portal. To do that, follow these steps:

1. Navigate to the listener where you have the expired or soon-to-be expired certificate.
2. Select the **Renew or edit the selected certificate** option.
3. In the **Choose certificate** option, you can choose between uploading a renewed certificate or choose a certificate from your Key Vault.
4. Select **Save** once done.

You can also renew SSL certificates by using Azure PowerShell or Azure CLI. For information, see [Renew Application Gateway certificates](https://docs.microsoft.com/azure/application-gateway/renew-certificates).

## **Recommended Documents**

- [TLS termination and end to end TLS with Application Gateway overview](https://docs.microsoft.com/azure/application-gateway/ssl-overview)
