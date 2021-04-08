<properties
  pagetitle="ASC/Certificate Key Vault Binding/Link"
  service="microsoft.certificateregistration"
  resource="certificateorders"
  ms.author="curibe,shrahman"
  selfhelptype="Generic"
  supporttopicids="32604392"
  resourcetags=""
  productpesids="16512"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="9628bbb6-fedd-4f5f-ab9a-c97c64099a59"
  ownershipid="Compute_AppService" />
# ASC/Certificate Key Vault Binding/Link

## **Recommended Steps**

* **How do I import a certificate from Key Vault?**

   For instructions, [see this document](https://docs.microsoft.com/azure/app-service/configure-ssl-certificate#import-a-certificate-from-key-vault)


* **I get the error "Another certificate exists with same thumbprint XXXX at location XXXX in the Resource Group XXXX". What does this mean?**

   Certificates live inside a WebSpace (a virtual boundary where App Service Plans are created). Therefore, all AppServicePlans within a WebSpace will share certificates and we do not need to upload the same certificate again if it has to be used on a website that is within same webspace.

* **What permissions are required on Key Vault for App Service Certificate?**

|Service Principal|Secret Permissions|Certificates|
|--|--|--|
|Microsoft Azure App Service|Get  | Get |
|Microsoft.Azure.CertificateRegistration|Get, List, Set, Delete | Get, List|


## **Recommended Documents**

* [Rekey (Sync) a Certificate](https://azure.github.io/AppService/2018/02/20/Troubleshooting-Tools-for-App-Service-Certificate.html)
