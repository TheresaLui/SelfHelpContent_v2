<properties
  pagetitle="ASC/Domain Verification taking too long or not completing"
  service="microsoft.certificateregistration"
  resource="certificateorders"
  ms.author="shrahman"
  selfhelptype="Generic"
  supporttopicids="32690925"
  resourcetags=""
  productpesids="16512"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="eeb97967-9e08-47fc-8fd2-a9052fa10290"
  ownershipid="Compute_AppService" />
# ASC/Domain Verification taking too long or not completing

## **Recommended Steps**

**What do the certificate statuses mean as shown by diagnostics?**

- **Issued** - Certificate is issued and ready for use.

- **Pending Issuance** - Certificate issuance is pending on domain ownership verification by customer.

- **Denied** - Certificate renewal failed as domain ownership verification was not completed within 45 days. The certificate will be valid till its expiration date and then revoked. Customer need to request for a new certificate.

**What can I check if domain verification is not completing?**
 
 * Select the **Verify** button to open the Domain Verification window
 * At the top, the Domain Verification Token appears. This is a randomly generated identifier that helps in the verification process.
 
 There are three ways to validates domain ownership:

   1. HTML file: Host an HTML file at the root of the webserver hosting the domain
   2. DNS TXT record: Create a TXT record for the root domain
   3. Email: Select the verification link included in the mail sent to the email addresses associated with the domain

 For more details about each option, please see the following [blog](https://azure.microsoft.com/blog/internals-of-app-service-certificate/).
