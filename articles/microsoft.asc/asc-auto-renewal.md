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

### What can I check if certificate doesn't auto-renew?

- Check if the certificate expiration date is within 60 days.

- Determine if the Key Vault has required permissions for auto-renewal to work. Add the following permissions to the Key Vault Access Policy for the service principals in question:

|Service Principal|Secret Permissions|Certificates | 
|--|--|--
|Microsoft Azure App Service|Get|Get|
|Microsoft.Azure.CertificateRegistration|Get,List,Set,Delete|Get,List|
		
- Determine whether domain ownership verification is pending. Most App Service Certificates renew with no requirement to verify domain ownership. For some certificate renewals, GoDaddy requires domain verification within 45 days. In this case, users must add the new token to their DNS records. If the TXT records are not set within the 45 days, certificate renewal will be denied. The certificate will be valid for another 15 days until the certificate expiration date.

    To manually verify your domain ownership by adding a TXT record:
    * Go to the Domain Name Service (DNS) provider that hosts your domain name.
    * Add a TXT record for your domain that uses the value of the domain token that's shown in the Azure portal.
   <br>

### What do the certificate statuses mean as shown by diagnostics?

- **Issued** - Certificate is issued and ready for use.

- **Pending Issuance** - Certificate issuance is pending on domain ownership verification by customer.

- **Denied** - Certificate renewal failed as domain ownership verification was not completed within 45 days. The certificate will be valid until its expiration date and then revoked. The customer will need to request a new certificate.


### Why is my certificate issued for 11 months and not for a full year?<br>

For all certificates issued after 9/1/2020, the maximum duration is now 397 days. Certificates issued before 9/1/2020 have a maximum validity of 825 days until they are renewed, rekeyed etc. Any certificate renewed after 9/1/2020 will be affected by this change and users may notice a shorter validity on their renewed certificates. 
<br>
GoDaddy has implemented a subscription service that both meets the new requirements while honoring existing customer certificates. Thirty days before the newly-issued certificate expires, the service automatically issues a second certificate that extends the duration to the original expiration date. 
App Service is working with GoDaddy to address this change and make sure that our customers receive the full duration of their certificates.

## **Recommended Documents**

* [My SSL certificate is not being auto-renewed](https://azure.github.io/AppService/2017/07/24/FAQ-SSL-certificates-for-Web-Apps-and-App-Service-Certificates#auto-renew)
* [Troubleshooting Tools for App Service Certificate](https://azure.github.io/AppService/2018/02/20/Troubleshooting-Tools-for-App-Service-Certificate.html)
