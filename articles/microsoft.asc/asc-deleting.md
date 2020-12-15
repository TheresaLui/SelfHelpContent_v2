<properties
  pagetitle="ASC/Deleting"
  service="microsoft.certificateregistration"
  resource="certificateorders"
  ms.author="curibe,shrahman"
  selfhelptype="Generic"
  supporttopicids="32690926"
  resourcetags=""
  productpesids="16512"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="fc925934-4c50-4a81-8e78-f582059e69dc"
  ownershipid="Compute_AppService" />
# ASC/Deleting

## **Recommended Steps**

**How do I retrieve a deleted certificate?**
There is no option to retrieve a deleted certificate. Once the App Service certificate is deleted, it will be deleted at GoDaddy also and GoDaddy will mark this certificate as revoked. Therefore, this certificate cannot be used anymore and you need to purchase a new certificate.

**How do I request for refund of deleted certificate?**
App Service certificate will be billed only when the certificate is in Issued state. If the certificate is in Pending state, you can delete it without getting charged. However, as soon as the certificate is issued and the state is moved to Issued state, there is no option to get a refund.

**I am getting this error "Delete for 'XXXX' App Service Certificate failed because there are still imported certificates derived from the App Service Certificate in the source subscription". What does that mean?**
This means this certificate is used by HTTPS binding on one of the Web Apps. Please remove HTTPS bindings from the Web App and then try to delete the certificate.

**I am getting this error "Cannot remove certificate with thumbprint XXXX because it is used for hostname XXXX". What does that mean?**
This means this certificate is used by HTTPS binding on one of the Web Apps. Please remove HTTPS bindings from the Web App and then try to delete the certificate.