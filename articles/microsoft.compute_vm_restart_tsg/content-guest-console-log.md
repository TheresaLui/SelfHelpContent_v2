<properties
	pageTitle="How to collect guest OS logs"
	description="How to collect guest OS logs"
	service="microsoft.compute"
	resource="Microsoft.Compute/virtualMachines"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="928cccb4-1dc5-4eb0-b3d7-5f6535a109d5"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to collect guest OS logs

1. Validate if Guest OS logs should be collected (prerequisites: no logs already collected and approval from the customer to collect the GuestOS Logs
2. The following types of logs should be collected: Console Log, WinGuestAnalyzer and InspectIaaSDisk log

**Note:** Even if running HA or collecting the Guest OS logs might be necessary at a later moment, please keep in mind that our data/log retention policy, from platform side, can be very short. Hence, our recommendation is to collect both HA and Guest OS logs at the sooner.
