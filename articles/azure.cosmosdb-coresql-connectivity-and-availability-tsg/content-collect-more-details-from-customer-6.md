<properties
	  pageTitle="Collect more details from customer"
	  description="Collect more details from customer"
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
	  articleId="85317970-a2b8-4489-b44f-6879d585b201"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Collect more details from customer

Collect the following details from customer to troubleshoot the unavailability issue:

##What questions to ask and data collection
* DocumentServiceId
* Full Exception Trace with the message
* Region where documentclient is running
* Connectivity mode: Gateway or Direct (This is specified in connect policy which is supplied in constructor of Document client Default is gateway)
* Number of VMs ?at which exception was seen during the time
* Number of service unavailable exceptions
* Duration of failure
* Complete stack traces for at least 20 exceptions in a flat file

If no enough details, please provide customer with customer ready message for minimum required details to start the case.

