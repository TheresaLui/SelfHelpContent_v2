<properties
	pageTitle="Error configuring a new appliance"
	description="Error configuring a new appliance troubleshooting"
	infoBubbleText="See details on the right"
	service="microsoft.storsimple"
	resource="managers"
	authors="Archana-MSFT"
	ms.author="armukk"
	displayOrder=""
	articleId="bcdc2eb5-d394-4b8d-8f1d-6faaa1143bb0"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32630502"
	resourceTags="8000Series"
	productPesIds="15438"	
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>

# Error configuring a new appliance 

## **Recommended Steps**

If the `Invoke-HcsSetupWizard` command is failing while validating DNS with message *Could not validate the DNS server. Ensure you have entered a valid DNS server, the server is reachable and UDP 53 is open for outbound communication* and you have already validated the DNS IP address as communicated in the message and are still facing the same issue, please bypass validation by using the command `Invoke-HcsSetupWizard -BypassValidation 1` to successfully run the setup wizard.

## **Recommended Documents**

- [Deploy your on-premises StorSimple device](https://docs.microsoft.com/azure/storsimple/storsimple-8000-deployment-walkthrough-u2)<br>
- [CHAP configuration](https://docs.microsoft.com/azure/storsimple/storsimple-8000-configure-chap)
- [Networking requirements for the StorSimple Device](https://docs.microsoft.com/azure/storsimple/storsimple-8000-system-requirements#networking-requirements-for-your-storsimple-device)

