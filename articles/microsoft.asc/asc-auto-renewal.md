<properties
  pagetitle="ASC/Auto-renewal"
  service="microsoft.certificateregistration"
  resource="certificateorders"
  ms.author="shrahman"
  selfhelptype="Generic"
  supporttopicids="32604391"
  resourcetags=""
  productpesids="16512"
  cloudenvironments="blackforest,fairfax,public,usnat,ussec,mooncake"
  disableclouds=""
  articleid="eaa907cb-1571-48f7-9a8a-f925442c5d51"
  ownershipid="Compute_AppService" />
# ASC/Auto-renewal

## **Recommended Steps**
**What can I check if certificate is not auto-renewed?**

- Check if certificate expiration date is within 60 days.

- Check if the KeyVault has required permissions for auto-renewal to work. Give the Key Vault Access Policy following permissions on given service principals:

  |Service Principal|Secret Permissions|Certificates | 
|--|--|--
|Microsoft Azure App Service|Get|Get|
|Microsoft.Azure.CertificateRegistration|Get,List,Set,Delete|Get,List|
		
- Check if domain ownership verification is pending. Most of the time App Service Certificates will be renewed without any need to verify domain ownership. But for few cert renewals, GoDaddy needs domain verification and users have to add the new token into their DNS records. GoDaddy will wait for 45 days for domain verification. If the TXT records is not set within the 45 days, certificate renewal will be denied. But the certificate will still be valid for another 15 days till the certificate expiration date.

- Manually verify your domain ownership by adding a TXT record:

  - Go to the Domain Name Service (DNS) provider that hosts your domain name.

  - Add a TXT record for your domain that uses the value of the domain token that's shown in the Azure portal.

**What do the certificate statuses mean as shown by diagnostics?**

- **Issued** - Certificate is issued and ready for use.

- **Pending Issuance** - Certificate issuance is pending on domain ownership verification by customer.

- **Denied** - Certificate renewal failed as domain ownership verification was not completed within 45 days. The certificate will be valid till its expiration date and then revoked. Customer need to request for a new certificate.

**Why is my certificate issued for 11 months only and not for a year?**
The industry has recently adopted a campaign to reduce the maximum certificate duration from 825 days to 397 days, 
which applies to any certificate issued after 9/1/2020. Certificates issued prior to 9/1/2020 can still have a 
maximum validity of 825 days until they are renewed, rekeyed etc. Any certificate renewed after 9/1/2020 will be 
effected by this change and users may notice a shorter validity on their renewed certificates. 
In order to meet this new requirement and still give users the full duration on their certificates, GoDaddy has 
implemented a subscription service. This service is aware of the customer’s certificate’s original expiration date. 
30 days before the newly issued certificate expires (the earlier expiration) they will automatically issue a second 
certificate which will be valid from that date until the original expiration date to account for the remaining time. 
Rest assured that App Service is working with GoDaddy to address this change to make sure that our customers still 
get the full duration of their certificates.