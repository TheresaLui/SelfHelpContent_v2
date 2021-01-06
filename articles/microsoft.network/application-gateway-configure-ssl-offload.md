<properties
    pageTitle="Configure SSL offload"
    description="Configure SSL offload"
    service="microsoft.network"
    resource="applicationgateways"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder=""
    selfHelpType="resource"
    articleId="7640a487-6f9f-4a3c-9e53-5c75862cc1f4"
    resourceTags=""
    productPesIds="15922"
    supportTopicIds="32783364"
    cloudEnvironments="public, fairfax, mooncake, blackforest, ussec, usnat"
 />

# Configure SSL offload

## **Recommended Steps**

SSL offload or SSL termination enables you to offload the SSL encryption and decryption of your traffic to the Application Gateway and have the decrypted traffic forwarded to your backend servers. By using this, you can avoid the overhead of encryption and decryption on your backend servers and they can just cater to their application requirements.

SSL offload is mostly done where the connection from client to Application Gateway is exposed over the internet and the connection from Application Gateway to the backend servers are mostly private where SSL re-encryption might not be needed. SSL is always terminated at the Application Gateway level.

You can configure SSL offload by following a few quick steps:

- Make sure your listener is using HTTPS protocol.
- Upload your SSL certificate in the listener in .pfx format or referencing it from your Key Vault.
- Make sure the protocol in HTTP settings is HTTP.

Note that the SSL certificate uploaded in the listener can be a local .pfx file or if you are using a v2 SKU gateway (Standard_v2/WAF_v2), then you have an option to reference the certificate uploaded in your Key Vault directly from Application Gateway. Using the Key Vault integration also enables auto-renewal of certificates, where Application Gateway polls KV to check for a newer version of the certificate every 4 hours.

## **Recommended Documents**

- [TLS termination and end to end TLS with Application Gateway Overview](https://docs.microsoft.com/azure/application-gateway/ssl-overview#tls-termination)
- [Configure an application gateway with TLS termination using the Azure portal](https://docs.microsoft.com/azure/application-gateway/create-ssl-portal)
- [Create an application gateway with TLS termination using Azure PowerShell](https://docs.microsoft.com/azure/application-gateway/tutorial-ssl-powershell)
- [Create an application gateway with TLS termination using the Azure CLI](https://docs.microsoft.com/azure/application-gateway/tutorial-ssl-cli)
- [TLS termination with Key Vault certificates](https://docs.microsoft.com/azure/application-gateway/key-vault-certs)
