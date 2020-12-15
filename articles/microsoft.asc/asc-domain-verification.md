<properties
  pagetitle="ASC/Domain Verification taking too long or not completing&#xD;"
  service="microsoft.certificateregistration"
  resource="certificateorders"
  ms.author="curibe,shrahman"
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

 In order to acquire an ASC, you need to verify that you own the domain included in the request:
 
 * Click on the "Verify" button to open the Domain Verification window
 * At the top, you would see a Domain Verification Token which is a randomly generated identifier that helps in the verification process
 
 There three ways to validates domain ownership:

1. HTML file: Host an HTML file at the root of the webserver hosting the domain
2. DNS TXT record: Create a TXT record for the root domain
3. Email: Click on the verification link included in the mail sent to the Email addresses associated with the domain

For more details about each option, please see the following [blog](https://azure.microsoft.com/blog/internals-of-app-service-certificate/).