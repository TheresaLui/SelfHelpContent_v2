<properties
	  pageTitle="Check if the activity exist in the audit log of the source app"
	  description="Check if the activity exist in the audit log of the source app"
      service="Microsoft.Security"
      resource="Microsoft.Security/alerts"
	  authors="rimayber"
	  ms.author="rimayber"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="21d573c8-928c-4427-97a1-9155c2bb918e"
	  ownershipId="CloudAppSecurity_API"
/>

# Check if the activity exist in the audit log of the source app

1. Customer should check if the missing activities in MCAS exist on the audit of the source app. 
2. For O365 apps, the customer should take the logs from https://protection.office.com/unifiedauditlog. 
3. If you are unaware of the source, please engage SRE/SME (AVA) through the Swarming channel, to determine the correct source