<properties
	pageTitle="Unable to register the device"
	description="Unable to register the device troubleshooting"
	infoBubbleText="See details on the right"
	service="microsoft.storsimple"
	resource="managers"
	authors="Archana-MSFT"
	ms.author="armukk"
	displayOrder=""
	articleId="236d5cf5-cf31-4866-8a2c-535309710eaf"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32630510"
	resourceTags="8000Series"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# Unable to register the device 

## **Recommended Steps**

If the `Invoke-HcsSetupWizard` command is failing while validating DNS with message *Could not validate the DNS server. Ensure you have entered a valid DNS server, the server is reachable and UDP 53 is open for outbound communication* and you have already validated the DNS IP address as communicated in the message and are still facing the same issue, please bypass validation by using the command `Invoke-HcsSetupWizard -BypassValidation 1` to successfully run the setup wizard.

## **Recommended Documents**

* [Deploy your on-premises StorSimple device](https://docs.microsoft.com/azure/storsimple/storsimple-8000-deployment-walkthrough-u2)<br>

