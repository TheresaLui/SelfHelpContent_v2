<properties
    pageTitle="Upload authentication or trusted root certificate"
    description="Upload authentication or trusted root certificate"
    service="microsoft.network"
    resource="applicationgateways"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder="38"
    selfHelpType="resource"
    articleId="7640a487-6f9f-4a3c-9e53-5c75862cc1f8"
    resourceTags=""
    productPesIds="15922"
    supportTopicIds="32783367"
    cloudEnvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
    ownershipId="CloudNet_AzureApplicationGateway"
/>

# Upload authentication or trusted root certificate

## **Recommended Steps**

To perform end-to-end TLS, Application Gateway requires backend instances to be allowed by uploading authentication or trusted root certificates. For the v1 SKU, authentication certificates are required, and for the v2 SKU, trusted root certificates are required, to allow the backend servers.

For v1 SKU (Standard/WAF): Authentication certificates are the public key of the backend server certificate. Authentication certificates are not needed for trusted backend services, such as Web Apps.

For v2 SKU (Standard_v2/WAF_v2): Trusted root certificates are the root certificate of the backend server certificate. Trusted root certificates are not needed for well-known CAs, such as DigiCert. Make sure that the Hostname in HTTP settings matches with the CN of your certificate.

To upload an authentication certificate or trusted root certificate, follow these steps:

1. Navigate to your HTTP settings and make sure that the protocol is set as HTTPS.
2. If you are using v1 SKU, you can choose the **create new** option to upload a `.cer` certificate file, which is the public key of your backend server certificate. Make sure the thumbprint matches. Or you can choose an existing certificate. If the backend server is a trusted Azure service, such as Azure App Service/Web Apps, you can choose the **Use for App Service** option, and you don't need to upload a certificate.
3. If you are using v2 SKU, you can choose the **create new** option to upload a `.cer` certificate file, which is the root certificate of your backend server certificate. Or you can choose an existing certificate from the list. If your backend server certificate is signed by a well-known CA, such as Digicert, you can choose the **Use well known CA certificate**, and you don't need to upload a certificate. If your backend certificate is self-signed or not well-known, then you'll have to upload the root certificate.

## **Recommended Documents**

- [Create certificates to allow the backend with Azure Application Gateway](https://docs.microsoft.com/azure/application-gateway/certificates-for-backend-authentication)
- [Generate an Azure Application Gateway self-signed certificate with a custom root CA](https://docs.microsoft.com/azure/application-gateway/self-signed-certificates)
