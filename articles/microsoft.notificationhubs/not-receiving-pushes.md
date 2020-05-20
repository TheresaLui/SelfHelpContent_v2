<properties
	pageTitle="I don't see any errors but my devices are not receiving pushes"
	description="I don't see any errors but my devices are not receiving pushes"
	service="microsoft.notificationhubs"
	authors="locphan"
	displayOrder="1"
	selfHelpType="resource"
	resource="namespaces"
	resourceTags="notificationHubs"
	productPesIds=""
	supportToicIds =""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="0fd1aa3f-574c-46ca-92e2-93a57c63cc92"
	ownershipId="AzureNotificationHubs"
/>

# I don't see any errors but my devices are not receiving pushes

## **Recommended steps**
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
