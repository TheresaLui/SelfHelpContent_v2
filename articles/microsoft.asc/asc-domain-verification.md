<properties
	pageTitle="ASC/Domain Verification taking too long or not completing"
	description="ASC/Domain Verification taking too long or not completing"
	service="microsoft.asc"
	resource="asc"
	authors="cts-shrahman, cristhianu"
    ms.author="shrahman,curibe"
	displayOrder="6"
	selfHelpType="generic"
	supportTopicIds="32690925"
	resourceTags=""
	productPesIds="16512"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="eeb97967-9e08-47fc-8fd2-a9052fa10290"
	ownershipId="Compute_AppService"
/>

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
