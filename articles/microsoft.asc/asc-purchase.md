<properties
  pagetitle="ASC/Purchasing"
  service="microsoft.certificateregistration"
  resource="certificateorders"
  ms.author="curibe,shrahman"
  selfhelptype="Generic"
  supporttopicids="32604397"
  resourcetags=""
  productpesids="16512"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="0b88631b-2f80-4b01-b326-d1190cb344e6"
  ownershipid="Compute_AppService" />
# ASC/Purchasing

## **Recommended Steps**
**I have mistakenly purchased an SSL certificate for the wrong domain. Can I get a refund?**

The App Service certificate will be billed only when the certificate is in an Issued state. If the certificate is in a Pending Issuance state, you can delete it without getting charged. However, as soon as the certificate is in an Issued state, there is no option to get a refund.

**What do certificate statuses mean, as shown by diagnostics?**

* Issued - Certificate is issued and ready for use.
* Pending Issuance - Certificate issuance is pending on domain ownership verification by customer.
* Denied - Certificate renewal failed because domain ownership verification was not completed within 45 days. The certificate will be valid until its expiration date and then revoked. The customer needs to request a new certificate.
	
**What can I check if domain verification is not completing?**

There are three ways to do domain verification. If one of these options isn't working, try the others:

* HTML file: Host an HTML file at the root of the web server hosting the domain.
* DNS TXT record: Create a TXT record for the root domain.
* Email: Click the verification link included in the mail sent to the email addresses associated with the domain.

For details steps on each of the preceding methods, see [this blog](https://azure.microsoft.com/blog/internals-of-app-service-certificate/).


## **Recommended Documents**

* [Unable to purchase an SSL certificate or App Service certificate](https://azure.github.io/AppService/2017/07/24/FAQ-SSL-certificates-for-Web-Apps-and-App-Service-Certificates#how-do-i-purchase-and-configure-a-new-ssl-certificate-in-azure-for-my-web-app)
* [Buying and configuring an SSL certificate for Azure App Service](https://docs.microsoft.com/azure/app-service/web-sites-purchase-ssl-web-site)