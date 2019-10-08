<properties
  	pageTitle="TSG Content Step: Check if there is a custom probe"
	  description="TSG Content Step: Check if there is a custom probe"
	  service="microsoft.network"
	  resource="applicationGateway"
	  authors="JRMayberry"
	  ms.author="rimayber"
	  displayOrder=""
	  selfHelpType="TSG_Description"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
	articleId="82af8570-2d65-4710-847a-7de2e1617468"
/>

**How to check if there is a custom probe configured:**

1. Go to the *Backend HTTP Settings Collection* in ASC and select the appropriate HTTP Setting that is configured in your rule
2. Check the Probe field, if there is a probe mentioned, then the customer is using a custom probe
