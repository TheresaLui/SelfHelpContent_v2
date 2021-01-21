<properties
    pageTitle="Configure SSL offload"
    description="Configure SSL offload"
    service="microsoft.network"
    resource="applicationgateways"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder="34"
    selfHelpType="resource"
    articleId="7640a487-6f9f-4a3c-9e53-5c75862cc1f4"
    resourceTags=""
    productPesIds="15922"
    supportTopicIds="32783364"
    cloudEnvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
    ownershipId="CloudNet_AzureApplicationGateway"
/>

# Configure SSL offload

## **Recommended Steps**

SSL offload (also called *SSL termination*) enables you to offload SSL encryption and decryption of your traffic to the Application Gateway. The decrypted traffic is then forwarded to your backend servers. This solution eliminates the overhead of encryption and decryption on your backend servers so that they can fulfill their application requirements.

SSL offload is mostly done where the connection from client to Application Gateway is exposed over the internet and the connection from Application Gateway to the backend servers is mostly private (i.e., SSL re-encryption might not be needed). SSL is always terminated at the Application Gateway level.

To configure SSL offload:

- Make sure your listener uses HTTPS protocol
- Upload your SSL certificate in the listener in .pfx format or reference it from your Key Vault
- Make sure the protocol in HTTP settings is **HTTP**

Note that the SSL certificate uploaded in the listener can be a local .pfx file. Or, if you use a v2 SKU Gateway (Standard_v2/WAF_v2), you have an option to reference the certificate uploaded in your Key Vault directly from Application Gateway. Key Vault integration enables certificate auto-renewal, where Application Gateway polls KV to check for a newer version of the certificate every 4 hours.

## **Recommended Documents**

- [TLS termination and end-to-end TLS with Application Gateway Overview](https://docs.microsoft.com/azure/application-gateway/ssl-overview#tls-termination)
- [Configure an application gateway with TLS termination using the Azure portal](https://docs.microsoft.com/azure/application-gateway/create-ssl-portal)
- [Create an application gateway with TLS termination using Azure PowerShell](https://docs.microsoft.com/azure/application-gateway/tutorial-ssl-powershell)
- [Create an application gateway with TLS termination using the Azure CLI](https://docs.microsoft.com/azure/application-gateway/tutorial-ssl-cli)
- [TLS termination with Key Vault certificates](https://docs.microsoft.com/azure/application-gateway/key-vault-certs)
