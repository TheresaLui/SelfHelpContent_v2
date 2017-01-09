<properties
	pageTitle="Issues with Devices or Notifications/Registration disappears"
	description="Issues with Devices or Notifications/Registration disappears"
	service="microsoft.notificationhubs"
	authors="faridabharmal"
	displayOrder=""
	selfHelpType="Generic"
	resource="namespaces"
	resourceTags="notificationHubs"
	productPesIds="15973"
	supportToicIds ="32565574"
	cloudEnvironments="public"
/>

# Issues with Devices or Notifications/Registration disappears

## **Recommended steps**
Registration disappearance is generally caused by invalid PNS handle or invalid token.<br>

* Verify [Push Notification Services](data-blade:Microsoft_Azure_NotificationHubs.NotificationHubServices) credentials are correctly configured.<br>
* Verify Push Notification Services credential mode and app mode are both either sandbox or production.<br>
* Verify that you register with Notification Hubs whenever you get the latest token since devices with expired tokens are deleted.<br>

## **Recommended documents**
* [Diagnosis guidelines](http://go.microsoft.com/fwlink/?LinkID=824681)<br>