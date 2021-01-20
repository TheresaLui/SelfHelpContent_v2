<properties
  pagetitle="ASC/Renewing-Rekeying&#xD;"
  service="microsoft.certificateregistration"
  resource="certificateorders"
  ms.author="curibe,shrahman"
  selfhelptype="Generic"
  supporttopicids="32604398"
  resourcetags=""
  productpesids="16512"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="8b046fe6-615a-42b7-a8fd-8b61020ddddf"
  ownershipid="Compute_AppService" />
# ASC/Renewing-Rekeying

## **Recommended Steps**


**How to Rekey?**

See [these instructions](https://docs.microsoft.com/azure/app-service/web-sites-purchase-ssl-web-site#rekey-certificate).

**How to Renew?**

See [these instructions](https://docs.microsoft.com/azure/app-service/web-sites-purchase-ssl-web-site#renew-certificate).

**What permissions are required on Key Vault for App Service Certificate?**

|Service Principal|Secret Permissions|Certificates|
|--|--|--|
|Microsoft Azure App Service|Get|Get|
|Microsoft.Azure.CertificateRegistration|Get,List,Set,Delete|Get,List|

**Our App Certificate was expired. Can it be renewed with the same thumbprint?**

It is not possible to renew an expired certificate. You need to create a new certificate, which will have a different thumbprint.

## **Recommended Documents**

[FAQ SSL certificates for Web Apps and App Service Certificates](https://azure.github.io/AppService/2017/07/24/FAQ-SSL-certificates-for-Web-Apps-and-App-Service-Certificates.html).