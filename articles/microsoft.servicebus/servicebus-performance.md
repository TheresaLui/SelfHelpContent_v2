<properties
  pagetitle="Performance or latency issues"
  description="performance"
  service="microsoft.servicebus"
  resource="namespaces"
  ms.author="chiragpa,aschhab"
  selfhelptype="Generic"
  supporttopicids="32633389"
  resourcetags=""
  productpesids="13186"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="97f3479b-2531-466a-b6b9-524326284469"
  ownershipid="AzureMessaging_Common" />
# Performance or latency issues

Perceived performance on Azure Service Bus depends on a variety of factors, including: 

  * Pricing tier for your namespace (Standard or Premium)
     * Standard tier namespaces are a multi-tenant setup
     * Premium tier namespaces have dedicated resources allocated per namespace

  * Enterprise message features in use
     * Message payload size
     * Transactions
     * Sessions
     * Scheduled messages

We encourage you to follow the guidance in the [best practices document](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-performance-improvements) to improve the performance.

You may also consider scaling the resources allocated to the namespace -
  * If the namespace is on the Standard tier, consider [migrating to Premium](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-migrate-standard-premium).
  * If the namespace is on the Premium tier, consider [scaling up the messaging units allocated to the namespace](https://docs.microsoft.com/azure/service-bus-messaging/automate-update-messaging-units).

## **Recommended Documents**

* [Best practices for performance improvements using Service Bus Messaging](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-performance-improvements)<br>
* [Automatically update Messaging Units for Azure Service Bus Premium](https://docs.microsoft.com/azure/service-bus-messaging/automate-update-messaging-units)
* [Migrate Standard namespaces to Premium](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-migrate-standard-premium)
