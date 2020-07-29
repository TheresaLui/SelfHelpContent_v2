<properties
	pageTitle="Check if the error failed due to a partner dependency"
	description="Check if the error failed due to a partner dependency"
	service="microsoft.identity"
	resource=""
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="79ea66a5-20fa-42bc-970c-6e6d01706fd5"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if the error failed due to a partner dependency

* Use Kusto to find out whether the error was due to a failed request to one of the APIs that the Azure AD admin portal depends upon.
 
~~~kusto

// Confirm if the failure was due to a partner dependency call failing. Calls with responseCode >=400 signifies a failure 
Execute: [Web] [Desktop] [Web (Lens)] [Desktop (SAW)] https://idsharedwus.kusto.windows.net:443/ADIbizaUXWUS 
IfxPartnerNetworkCallScrubbed 
| where correlationId contains "<CorrelationId>"
| project env_time, partnerName, partnerRequestUrl, responseCode, sessionId

~~~
