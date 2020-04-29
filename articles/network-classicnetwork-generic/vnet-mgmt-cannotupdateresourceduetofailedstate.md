<properties
	pageTitle="management/cannotupdateresourcesduetofailedstate"
	description="management/cannotupdateresourcesduetofailedstate"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="anavinahar"
	ms.author="anavin"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584254"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="b5d4d6c8-ade4-4137-b4a1-8dc37b52d4d2"
	ownershipId="CloudNet_VirtualNetwork"
/>

# management/cannotupdateresourcesduetofailedstate

## **Recommended Steps**

Sometimes resources may show in failed state due to platform sync issues. You can follow steps below to resolve such issues:<br>

1. Open [Azure resource explorer](https://resources.azure.com)
2. Navigate to the desired resource in the left pane
3. Press Read/Write at the top of the page
4. Press Edit button
5. Press PUT button to sync the resource state
6. Try again to update the resource
