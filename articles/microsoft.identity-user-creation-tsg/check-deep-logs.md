<properties
	pageTitle="Check Kusto for request debugging"
	description="Check Kusto for request debugging"
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
	articleId="31ee5e34-2ba4-4b46-be96-6150cdad5770"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check Kusto for request debugging

* You can use Kusto to get more in-depth debugging of what happened for a particular request.

~~~kusto

// In-depth debugging of a call. A non-empty value in resultSignature signfies a failure.
https://idsharedwus.kusto.windows.net:443/ADIbizaUXWUS 
IfxDiagnosticsScrubbed 
| where correlationId contains "$CorrelationId$"
| project env_time, message, resultSignature 
| order by env_time asc

~~~
