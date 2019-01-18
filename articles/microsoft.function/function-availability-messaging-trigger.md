<properties
	pageTitle="Availability/Messaging function failed to trigger"
	description="Availability/Messaging function failed to trigger"
	service="microsoft.web"
	resource="functions"
	authors="cts-shrahman,shrahman"
    ms.author="shrahman, finbarr"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630468"
	resourceTags=""
	productPesIds="16072"
	cloudEnvironments="public"
/>

#  Availability/Messaging function failed to trigger

Common Scenarios:

1. The Function Runtime host is failing with an exception. <br>
2. The Function Host is not starting up. <br>
3. Another Function App is pulling messages in parallel. <br>
4. The Function App is idle due to no HTTP requests from the scale controller in the consumption plan or Always On is not enabled in the Dedicated plan.

