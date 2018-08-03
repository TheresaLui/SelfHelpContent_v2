<properties
	pageTitle="My devices/registrations disappeared from my hub after push."
	description="My devices/registrations disappeared from my hub after push."
	service="microsoft.notificationhubs"
	authors="locphan"
	displayOrder="6"
	selfHelpType="resource"
	resource="namespaces"
	resourceTags="notificationHubs"
	productPesIds=""
	supportToicIds =""
	cloudEnvironments="public, MoonCake"
/>

# My devices/registrations disappeared from my hub after push.

## **Recommended steps**
* Verify [Push Notification Services](data-blade:Microsoft_Azure_NotificationHubs.NotificationHubServices) credentials are correctly configured.<br>
* Verify Push Notification Services credential mode and app mode are both either sandbox or production.<br>
* Verify that you register with Notification Hubs whenever you get the latest token since devices with expired tokens are deleted.<br>
