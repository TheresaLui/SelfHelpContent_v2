<properties
	pageTitle="Issues with Devices or Notifications/Push notification not received"
	description="Issues with Devices or Notifications/Push notification not received"
	service="microsoft.notificationhubs"
	authors="faridabharmal"
	displayOrder=""
	selfHelpType="generic"
	resource="namespaces"
	resourceTags="notificationHubs"
	productPesIds="15973"
	supportTopicIds="32565573"
	cloudEnvironments="MoonCake"
/>

# Issues with Devices or Notifications/Push notification not received

## **Recommended steps**
The common causes are device is not online, device has bad network connectivity or device has invalid PNS handle.<br>
Notification Hub only guarantees send but does not guarantee deliver.

* Verify notification hub names used for registration, sends, and notification hub settings matched.<br>
* Verify the proper [SAS configuration strings](data-blade:Microsoft_Azure_NotificationHubs.AccessPolicyGridBlade) on client and backend.<br>
* Verify [Platform Notification System](data-blade:Microsoft_Azure_NotificationHubs.NotificationHubServices) credentials are correctly configured.<br>
* [Verify registrations](https://docs.azure.cn/notification-hubs/notification-hubs-push-notification-fixer#self-diagnose-tips) of all devices.<br>
* Verify devices are online via Wifi or data.<br>
* [Test Send](data-blade:Microsoft_Azure_NotificationHubs.TestSendBlade)<br>
* [Debug failed notifications](https://docs.azure.cn/notification-hubs/notification-hubs-push-notification-fixer#debug-failed-notifications-review-notification-outcome)<br>
* Use [Per Message Telemetry](https://msdn.microsoft.com/library/azure/mt608135.aspx)<br>

## **Recommended documents**
* [Diagnosis guidelines](https://docs.azure.cn/notification-hubs/notification-hubs-push-notification-fixer)<br>
* [Common error codes](https://msdn.microsoft.com/library/dn530751.aspx)<br>
* [Telemetry guide](https://msdn.microsoft.com/library/dn530751.aspx)<br>
