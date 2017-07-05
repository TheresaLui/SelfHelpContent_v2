<properties
	pageTitle="management/cannotupdateresourcesduetofailedstate"
	description="management/cannotupdateresourcesduetofailedstate"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584254"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public"
/>

# management/cannotupdateresourcesduetofailedstate

## **Recommended steps**
Sometimes resources may show in failed state due to platform sync issues. You can follow below steps to sync up the resources:<br>
1. Open [Azure resource explorer](https://resources.azure.com)<br>
2. Navigate to the desired resource in the left pane<br>
3. Press Read/Write at the top of the page<br>
4. Press Edit button<br>
5. Press PUT button to sync the resource state<br>
6. Try again to update the resource<br>