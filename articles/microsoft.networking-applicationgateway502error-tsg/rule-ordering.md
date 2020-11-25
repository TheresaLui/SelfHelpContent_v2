<properties
	pageTitle="TSG Content Step: Check rule ordering for AppGW v1 SKU"
  	description="TSG Content Step: Check rule ordering for AppGW v1 SKU"
  	service="microsoft.network"
  	resource="applicationGateway"
  	authors="JRMayberry"
    ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="977bb1cb-644f-4adc-923f-ee691507564d"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# Check rule ordering

**How to check rule ordering:**

If the AppGW is of v1 SKU, *rules are processed in the order of creation* and you can see the order in the portal. If a rule with basic listener is on top of the multi-site rules, then the basic rule might catch all the requests and send it to a different backend pool. If that backend pool turns out to be empty or unhealthy, AppGW will throw a 502 Bad Gateway error to the clients.

It is recommended to create the basic rule after the multi-site rules so that they take the top priority. To change the order of the rules, you have to **delete the basic rule and recreate it**. To do that, follow the steps below:

1. Click on the Request Routing Rules section of the Application Gateway in ASC
2. Check if there is a rule with a basic listener which is listed above the multi-site listener rules
3. Suggest the customer to delete the rule with the basic listener and create a new rule with the Basic listener so that it gets listed in the bottom and the multi-site rules are prioritized
