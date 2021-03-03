<properties
	  pageTitle="General approach"
	  description="General approach"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="ff9401ac-c775-4db6-8017-7ec555fb6844"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# General approach

Send email to customer with the following information: 

In the most common cases, client-side timeouts can be investigated through the public TSG https://docs.microsoft.com/azure/cosmos-db/troubleshoot-dot-net-sdk-request-timeout. 

Timeouts happen either because the backend request (Gateway or TCP) took longer than the **Request Timeout** the user configured for the SDK Client or because there are **connectivity issues** on the client-side. The most common sources for client-side connectivity issues are:

* **High CPU**: High CPU can cause connectivity problems due to resource exhaustion on the client-side. To confirm, we ask the user to capture the MAX CPU (not average) measured during the time of the incident. If MAX CPU usage is high (>60%) and the measurements show the increase correlates with the moment they see the Timeouts, this could be the reason. The user needs to investigate the source of CPU consumption.
* **Connection throttling** due to environment limits (SNAT port exhaustion for example), see https://docs.microsoft.com/en-us/azure/cosmos-db/troubleshoot-dot-net-sdk-request-timeout#socket-or-port-availability-might-be-low for each environment's (Azure VM, App Service, Functions, etc) recommendation.



