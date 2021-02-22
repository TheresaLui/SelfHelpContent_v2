<properties
	  pageTitle="Check if the customer has Scoped deployment configured on their end that might affect their activities visibility"
	  description="Check if the customer has Scoped deployment configured on their end that might affect their activities visibility"
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
	  articleId="5ab2b68b-9613-4fba-a899-b87eaf093cf2"
	  ownershipId="CloudAppSecurity_API"
/>

# Check if the customer has Scoped deployment configured on their end that might affect their activities visibility

1. Please ask the customer to check in Splunk if the customer has scoped deployment enabled on thier tenant that can exclude the impacted user
2. To do so, please use [Tenant Support Information](https://splunk-prod.cloudappsecurity.com:8000/app/search/supportengineer__tenant_information).
3. Include rules limit monitoring to users and apps defined in the rule. 
4. Exclude rules will cause CAS to not monitor activities from users and apps defined in the rule. 
5. Refer to this article for details [Scoped Deployment](https://docs.microsoft.com/cloud-app-security/scoped-deployment)
