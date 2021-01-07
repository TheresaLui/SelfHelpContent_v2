<properties
    pageTitle="Upload listener or SSL certificate"
    description="Upload listener or SSL certificate"
    service="microsoft.network"
    resource="applicationgateways"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder="37"
    selfHelpType="resource"
    articleId="7640a487-6f9f-4a3c-9e53-5c75862cc1f7"
    resourceTags=""
    productPesIds="15922"
    supportTopicIds="32783368"
    cloudEnvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
    ownershipId="CloudNet_AzureApplicationGateway"
/>

# Upload listener or SSL certificate

## **Recommended Steps**

To configure end-to-end SSL or SSL offload in Application Gateway, you must configure an HTTPS listener with an SSL certificate. You can upload a certificate to the HTTP listener in two ways:

1. If you are using v1 SKU (Standard/WAF), you can upload a .pfx file of your certificate from your local computer.
2. If you are using v2 SKU (Standard_v2/WAF_v2), you can either upload a .pfx file from your local drive, or you can integrate with certificates directly from your Key Vault with auto-renewal.

To upload a certificate to an existing listener or while creating a new listener using the Azure portal, follow these steps:

1. In the **Listener settings**, under **choose a certificate** option, select the **create new** option and choose between uploading a `.pfx` file or creating a reference to an existing certificate in your Key Vault.
2. If you choose to upload a `.pfx` certificate, you must provide the password for the same.
3. If you choose Key Vault integration, make sure that you create a user-assigned managed identity, that your Application Gateway has access to your Key Vault, and that it's not blocked by the firewall settings. For more information, see [TLS termination with Key Vault certificates](https://docs.microsoft.com/azure/application-gateway/key-vault-certs).

## **Recommended Documents**

- [Upload a certificate to the listener in Application Gateway using Azure portal](https://docs.microsoft.com/azure/application-gateway/create-ssl-portal#configuration-tab).
- [TLS termination and end-to-end TLS with Application Gateway overview](https://docs.microsoft.com/azure/application-gateway/ssl-overview)
