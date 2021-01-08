<properties
    pageTitle="Configure end-to-end SSL"
    description="Configure end-to-end SSL"
    service="microsoft.network"
    resource="applicationgateways"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder="33"
    selfHelpType="resource"
    articleId="7640a487-6f9f-4a3c-9e53-5c75862cc1f3"
    resourceTags=""
    productPesIds="15922"
    supportTopicIds="32783363"
    cloudEnvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
    ownershipId="CloudNet_AzureApplicationGateway"
/>

# Configure end-to-end SSL

End-to-end SSL enables you to secure your web traffic (from the client to Application Gateway, and from the Application Gateway to the back-end server) using TLS encryption.

## **Recommended Steps**

 To achieve end-to-end SSL encryption in Application Gateway, follow these steps:<br>
- Make sure your listener uses HTTPS protocol
- Upload your SSL certificate in the listener in .pfx format or reference it from your Key Vault
- Make sure the protocol in HTTP settings is **HTTPS**
- For back-end authentication: 
   - For v1 SKU (Standard/WAF), upload the public key of your back-end server certificate in .cer format so that Application Gateway identifies it as a valid back-end server. If the back-end server is a trusted Azure service, like Web Apps, no certificate upload is required. Instead, select **Use for App Service**.<br>
   - For v2 SKU, upload the root certificate of the back-end server certificate in .cer format. If the certificate is signed by a well-known CA, you don't have to upload the root certificate.

- Make sure the hostname entered in your HTTP settings or custom health probe matches the CN of your back-end server certificate.

|Listener  |Rule  |HTTP Settings  |
|---------|---------|---------|
|Protocol: HTTPS    | Basic or path-based rule|Protocol: HTTPS |
|Certificate: SSL certificate (PFX)    |Basic or path-based rule |Certificate: Authentication/Trusted Root (CER) |
|Certificate source:<br> v1: Local .pfx file upload with username and password|Basic or path-based rule |V1:<br> 1. Public key of back-end server certificate.<br> 2. Certificate not needed for trusted back-end services, e.g., Web Apps.|
|v2:<br>1. Local .pfx file upload with username and password.<br>2. Key Vault reference with option for auto-renewal.|Basic or path-based rule |V2:<br>1. Root certificate of the back-end server certificate. <br>2. Certificate not needed for well-known CAs, e.g, DigiCert.<br>3. Hostname must match with CN.|

## **Recommended Documents**

- [End-to-end TLS encryption in Application Gateway](https://docs.microsoft.com/azure/application-gateway/ssl-overview#end-to-end-tls-encryption)
- [Configure end-to-end TLS by using Application Gateway with the portal](https://docs.microsoft.com/azure/application-gateway/end-to-end-ssl-portal)
- [Configure end to end TLS by using Application Gateway with PowerShell](https://docs.microsoft.com/azure/application-gateway/application-gateway-end-to-end-ssl-powershell)
- [Integrate SSL certificates from Azure Key Vault in Application Gateway](https://docs.microsoft.com/azure/application-gateway/key-vault-certs)
