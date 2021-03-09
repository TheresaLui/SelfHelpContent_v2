<properties
	pageTitle="How to synchronize ARM subscription resources"
	description="How to synchronize ARM subscription resources"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="symondsk"
	ms.author="ksymonds"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="StorageMediaEdge_AccountManagement"
	articleId="c6a94863-6757-441b-838a-82e690a034fd"
/>

# How to synchronize ARM subscription resources

1. Navigate to Geneva Actions (Jarvis Actions) : [Azure Resource Manager >  Resource Synchronization > Synchronize Subscription resources from specific resource provider](https://jarvis-west.dc.ad.msft.net/B7BF0B48?genevatraceguid=b7ab48f0-5c87-405b-af1a-a01ad587b009)
2. Fill in the requested information and provide Resource Provider Namespace as "Microsoft.Storage"
3. Hit "Run".

You should see the details of the synchronization operation including a message like "Synchronization jobs started successfully"</br>
</br>


**<pre>Messages   Result   Preview</br></pre>**
**Synchronize Subscription resources from specific provider</br>**
<pre>
 1 {
 2 	"CorrelationId": "97454545-0cad-446c-9f93-e0c5edf8e53d",
 3 	"frontdoorLocation": "northcentralus",
 4 	"timestamp": "2019-01-18T00:38:30.9131462Z",
 5 	"message": "Synchronization jobs started successfully.",
 6	"data": {
 7		"subscriptionId": "6c34512345-3f5d-47e6-a123-1234567890",
 8		"targetNamespaces":[
 9			"Microsoft.Storage"
10			]
11		}
12 }

</pre>
</br>


