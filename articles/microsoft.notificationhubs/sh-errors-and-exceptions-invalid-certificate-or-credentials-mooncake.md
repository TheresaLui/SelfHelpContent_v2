<properties
	pageTitle="Errors and Exceptions/Invalid certificate or credentials"
	description="Errors and Exceptions/Invalid certificate or credentials"
	service="microsoft.notificationhubs"
	authors="faridabharmal"
	displayOrder=""
	selfHelpType="generic"
	resource="namespaces"
	resourceTags="notificationHubs"
	productPesIds="15973"
	supportTopicIds="32565582"
	cloudEnvironments="MoonCake"
/>

# Errors and Exceptions/Invalid certificate or credentials

## **Recommended steps**
* Verify [Push Notification Services](data-blade:Microsoft_Azure_NotificationHubs.NotificationHubServices) credentials are correctly configured.<br>
* (APNS) Verify exported keychain certificate contains only certificate instead of both key and certificate.<br>
* Enable Platform Notification Systems in various developer portals (e.g. enable GCM for Android in Google Developer, enable push in Apple Developer Center, link up Windows app with Windows Store, etc).<br>
* Enable push in client apps if applicable.<br>

## **Recommended documents**
* [Diagnosis guidelines](https://docs.azure.cn/notification-hubs/notification-hubs-push-notification-fixer)<br>
* [Common error codes](https://msdn.microsoft.com/library/dn530751.aspx)<br>
