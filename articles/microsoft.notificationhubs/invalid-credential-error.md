<properties
	pageTitle="I am getting 'Invalid credentials' or 'Failed to validate credentials' errors"
	description="I am getting 'Invalid credentials' or 'Failed to validate credentials' errors"
	service="microsoft.notificationhubs"
	authors="locphan"
	displayOrder="3"
	selfHelpType="resource"
	resource="namespaces"
	resourceTags="notificationHubs"
	productPesIds=""
	supportToicIds =""
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
	articleId="f57a3023-d98b-4bbd-9153-e09e1f182a27"
	ownershipId="AzureNotificationHubs"
/>

# I am getting 'Invalid credentials' or 'Failed to validate credentials' errors

## **Recommended steps**
* Verify [Push Notification Services](data-blade:Microsoft_Azure_NotificationHubs.NotificationHubServices) credentials are correctly configured.<br>
* (APNS) Verify exported keychain certificate contains only certificate instead of both key and certificate.<br>
* Enable Platform Notification Systems in various developer portals (e.g. enable GCM for Android in Google Developer, enable push in Apple Developer Center, link up Windows app with Windows Store, etc).<br>
* Enable push in client apps if applicable.<br>
