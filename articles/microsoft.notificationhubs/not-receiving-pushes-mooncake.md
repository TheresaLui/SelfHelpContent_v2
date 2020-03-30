<properties
    pageTitle="I don't see any errors but my devices are not receiving pushes"
    description="I don't see any errors but my devices are not receiving pushes"
    service="microsoft.notificationhubs"
    authors="locphan"
    ms.author="locphan"
    displayOrder="1"
    selfHelpType="resource"
    resource="namespaces"
    resourceTags="notificationHubs"
    productPesIds=""
    supportToicIds =""
    cloudEnvironments="MoonCake"
	articleId="89063f96-c32d-4d68-9102-5e7532d1126c"
	ownershipId="AzureMessaging_Common"
/>

# I don't see any errors but my devices are not receiving pushes

## **Recommended Steps**

* Verify that the notification hub names used for registration, sends, and notification hub settings match
* Verify the proper [SAS configuration strings](data-blade:Microsoft_Azure_NotificationHubs.AccessPolicyGridBlade) on client and backend
* Verify [Platform Notification System](data-blade:Microsoft_Azure_NotificationHubs.NotificationHubServices) credentials are correctly configured
* [Verify registrations](https://docs.azure.cn/notification-hubs/notification-hubs-push-notification-fixer#self-diagnose-tips) of all devices
* Verify devices are online via Wifi or data
* [Test Send](data-blade:Microsoft_Azure_NotificationHubs.TestSendBlade)
* [Debug failed notifications](https://docs.azure.cn/notification-hubs/notification-hubs-push-notification-fixer#debug-failed-notifications-review-notification-outcome)
* Use [Per Message Telemetry](https://msdn.microsoft.com/library/azure/mt608135.aspx)

## **Recommended Documents**

* [Diagnosis guidelines](https://docs.azure.cn/notification-hubs/notification-hubs-push-notification-fixer)<br>
* [Common error codes](https://msdn.microsoft.com/library/dn530751.aspx)<br>
* [Telemetry guide](https://msdn.microsoft.com/library/dn458821.aspx)<br>
