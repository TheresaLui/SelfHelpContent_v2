<properties
	pageTitle="How to synchronize ARM subscription resources"
	description="How to synchronize ARM subscription resources"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="Centennial_CloudNet_LoadBalancer"
	articleId="c6a94863-6757-441b-838a-82e690a034fd"
/>

# How to synchronize ARM subscription resources

1. Navigate to Geneva Actions (Jarvis Actions) : [Azure Resource Manager > Resource Group Management > Synchronize Subscription resources from specific resource provider](https://jarvis-west.dc.ad.msft.net/B7BF0B48?genevatraceguid=b7ab48f0-5c87-405b-af1a-a01ad587b009)
2. Fill in the requested information and provide Resource Provider Namespace as "Microsoft.Storage"
3. Hit "Run".
4. You should see the details of the synchronization operation including a message like "Synchronization jobs started successfully"
5. This will generally take about an hour to complete.
6. If required, you can monitor the progress by the correlationId returned.
7. The tables **traces** and **JobTraces** in **cluster("armprod.kusto.windows.net").database("ARMProd")** track the iterative sync operation.
