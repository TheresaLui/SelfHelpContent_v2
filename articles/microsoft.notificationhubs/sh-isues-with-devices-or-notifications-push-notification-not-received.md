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
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="18b1c3d4-db18-4739-899e-196608a15cb1"
	ownershipId="AzureNotificationHubs"
/>

# Issues with Devices or Notifications/Push notification not received

## **Recommended steps**
The common causes are device is not online, device has bad network connectivity or device has invalid PNS handle.<br>
Notification Hub only guarantees send but does not guarantee deliver.

* Verify notification hub names used for registration, sends, and notification hub settings matched.<br>
* Verify the proper [SAS configuration strings](data-blade:Microsoft_Azure_NotificationHubs.AccessPolicyGridBlade) on client and backend.<br>
* Verify [Platform Notification System](data-blade:Microsoft_Azure_NotificationHubs.NotificationHubServices) credentials are correctly configured.<br>
* [Verify registrations](http://go.microsoft.com/fwlink/?LinkID=824679) of all devices.<br>
* Verify devices are online via Wifi or data.<br>
* [Test Send](data-blade:Microsoft_Azure_NotificationHubs.TestSendBlade)<br>
* [Debug failed notifications](http://go.microsoft.com/fwlink/?LinkID=824680)<br>
* Use [Per Message Telemetry](http://go.microsoft.com/fwlink/?LinkID=824689)<br>

## **Recommended documents**
* [Diagnosis guidelines](http://go.microsoft.com/fwlink/?LinkID=824681)<br>
* [Common error codes](http://go.microsoft.com/fwlink/?LinkID=824682)<br>
* [Telemetry guide](http://go.microsoft.com/fwlink/?LinkID=824683)<br>
