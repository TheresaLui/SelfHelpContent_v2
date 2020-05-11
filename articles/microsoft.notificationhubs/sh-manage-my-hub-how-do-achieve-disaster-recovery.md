<properties
	pageTitle="Manage My Hub/How do I achieve disaster recovery"
	description="Manage My Hub/How do I achieve disaster recovery"
	service="microsoft.notificationhubs"
	authors="faridabharmal"
	displayOrder=""
	selfHelpType="generic"
	resource="namespaces"
	resourceTags="notificationHubs"
	productPesIds="15973"
	supportTopicIds="32565569"
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
	articleId="1643aeac-0b65-40c4-a4e3-815a4fd90fcf"
	ownershipId="AzureNotificationHubs"
/>

# Manage My Hub/How do I achieve disaster recovery

## **Recommended steps**
* Notification Hubs automatically conserve metadata, so after a brief downtime following the disaster, the hub metadata will recover and hub will be up and running with the same url and keys. 
* However, all device information will be lost. To recover device information, set up frequent export jobs for device data in order to backup their information. When the new hub is available, import device data to restore the hub’s full original state.

