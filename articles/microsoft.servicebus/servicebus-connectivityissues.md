<properties
  pagetitle="Connectivity issues"
  description="connectivity issues"
  service="microsoft.servicebus"
  resource="namespaces"
  ms.author="aschhab"
  selfhelptype="Generic"
  supporttopicids="32633395"
  resourcetags=""
  productpesids="13186"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="964de064-b70b-4486-b3c6-7fc620cc7e14"
  ownershipid="AzureMessaging_Common" />
# Connectivity issues

Client applications primarily connect with Azure Service Bus over the AMQP protocol. Connectivity issues tend to be one of two types: 

* Transient errors - If you've been able to connect with Azure Service Bus, but occasionally see errors that your application automatically recovers from with no impact to your data or business workflows, these issues might be caused by transient errors. The default retry policy built into the Azure Service Bus SDKs can help recover from these connectivity issues. If the issue persists for a long time, consider opening a support ticket.

* Configuration errors -  If you (or an administrator) recently made changes to the Azure Service Bus namespace and have seen connectivity issues since then, or if you have never been able to connect, these issues may be caused by configuration errors. 
   
   <br>Configuration errors can be related to the following: 
   * Port configuration
   * Virtual networks service endpoints - configuration
   * Firewall configuration
   * Private endpoints

   For configuration-related connectivity issues, refer to the following documentation. If the problem persists after reading these documents, open a support ticket.

## **Recommended Documents**

* [Which Ports should I open for Service Bus communication?](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-faq#what-ports-do-i-need-to-open-on-the-firewall)<br>
* [Connection troubleshooting document](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-troubleshooting-guide)<br>
* [Check if you can find the answer in our FAQ section!](https://azure.microsoft.com/documentation/articles/service-bus-faq/)<br>
* [Azure service status site](https://azure.microsoft.com/status/)<br>
* [Virtual Network service endpoints for Service Bus Premium tier](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-service-endpoints)<br>
* [Firewall - IP filtering for Service Bus Premium tier](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-ip-filtering)<br>
* [What IP addresses do I need to add to the allow list](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-faq#what-ip-addresses-do-i-need-to-add-to-allow-list)<br>
* [Private endpoints for Service Bus Premium tier](https://docs.microsoft.com/azure/service-bus-messaging/private-link-service)<br>
* [TLS](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-faq#is-it-possible-to-disable-tls-10-or-11-on-service-bus-namespaces)<br>
