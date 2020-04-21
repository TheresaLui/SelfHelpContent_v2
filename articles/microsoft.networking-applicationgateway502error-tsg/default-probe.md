<properties
	pageTitle="TSG Content Step: Check if backend server is acccessible for default probe"
  	description="TSG Content Step: Check if backend server is acccessible for default probe"
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
	articleId="83a7fcf2-0a9f-4887-b91e-308d1e1b6b62"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

**How to check if the backend server is accessible for default probe settings:**

1. Default probe will be on **<protocol>://127.0.0.1:<port>/** and accepts status codes **200-399**
2. The protocol and port will be inherited from the HTTP Settings
3. If the server is not accessible on localhost, ask the customer to [configure a custom probe](https://docs.microsoft.com/en-us/azure/application-gateway/application-gateway-create-probe-portal) with appropriate hostname and protocol and associate it to the backend HTTP settings that you are using
4. In case the backend server responds with a different status code that they want to be allowed, such as 401, mention it in the probe matching conditions.
