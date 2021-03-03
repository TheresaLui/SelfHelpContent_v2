<properties
  pagetitle="Connectivity issues"
  description="connectivity issues"
  service="microsoft.servicebus"
  resource="namespaces"
  ms.author="chiragpa,aschhab"
  selfhelptype="Generic"
  supporttopicids="32633395"
  resourcetags=""
  productpesids="13186"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="964de064-b70b-4486-b3c6-7fc620cc7e14"
  ownershipid="AzureMessaging_Common" />
# Connectivity issues

Client applications primarily connect with Azure Service Bus over the AMQP protocol. Connectivity issues may be of 2 kinds 

* Transient errors - If you have generally been able to connect with Azure Service Bus and occasionally see errors that your application recovers from automatically without any impact to your data or business workflows, then they may be transient errors. The default retry policy built into the Azure Service Bus SDKs can help recover from these connectivity issues. If the issue persists for a long time, please consider opening a support ticket.

* Configuration errors -  If you (or an administrator) recently made changes to the Azure Service Bus namespace and have seen connectivity issues since then, they may be caused by configuration errors. These could be related to any of the below 
   * Port configuration
   * Virtual networks service endpoints - configuration
   * Firewall configuration
   * Private endpoints

   For configuration related connectivity issues, please consider reading the below documentation. If the problem persists please open a support ticket.

## **Recommended Documents**

* [Which Ports should I open for Service Bus communication?](https://msdn.microsoft.com/library/mt723402.aspx)<br>
* [Service Bus TimeOutException](https://stackoverflow.com/questions/15345956/azure-service-bus-timeout)<br>
* [Check if you can find the answer in our FAQ section!](https://azure.microsoft.com/documentation/articles/service-bus-faq/)<br>
* [Azure service status site](https://azure.microsoft.com/status/)<br>
* [Virtual Network service endpoints](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-service-endpoints)<br>
* [Firewall - IP filtering](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-ip-filtering)<br>
* [Private endpoints](https://docs.microsoft.com/azure/service-bus-messaging/private-link-service)<br>