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

The following solutions help most customers who have issues with hostname binding not updating after the certificate auto-renews.

## What can I check if hostname binding is not updated after certificate auto-renewal?
The sync operation can takes up to 48 hours to update the hostname bindings. 

- To manually run a sync operation from the Azure portal, select **Certificate** > **Rekey and Sync** > **Sync**.

- Check the required permissions on Key Vault
	
  |Service Principal|Secret Permissions|Certificates|
  |--|--|--|
  |Microsoft Azure App Service|Get|Get|
  |Microsoft.Azure.CertificateRegistration|Get,List,Set,Delete|Get,List|

- Select the **Rekey** option to prompt a sync operation to update the binding. Rekeying your certificate will roll the certificate with a new certificate issued from the certificate authority. Certificate rekey operations are free and rekey does not incur additional charges.
