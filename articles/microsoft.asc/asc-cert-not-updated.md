<properties
  pagetitle="ASC/Renewing-Rekeying"
  service="microsoft.certificateregistration"
  resource="certificateorders"
  ms.author="curibe,shrahman"
  selfhelptype="Generic"
  supporttopicids="32693164"
  resourcetags=""
  productpesids="16512"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="578ffdca-6a2e-464e-85f0-fa70a6c34106"
  ownershipid="Compute_AppService" />
# ASC/Renewing-Rekeying

## **Recommended Steps**

**What can I check if hostname binding is not updated after certificate auto-renewal?**

- It takes upto 48 hours for sync operation to update the hostname bindings. So you can wait or try a manual Sync operation from portal: Certificate --> Rekey and Sync  -> Sync.

- Check required permissions on Keyvault
	
  |Service Principal|Secret Permissions|Certificates|
  |--|--|--|
  |Microsoft Azure App Service|Get|Get|
  |Microsoft.Azure.CertificateRegistration|Get,List,Set,Delete|Get,List|

- Try Rekey option and wait for sync operation to update the binding. Rekeying your certificate will roll the certificate with a new certificate issued from the certificate authority. Certificate rekey operations are free and rekey does not incur additional charges.