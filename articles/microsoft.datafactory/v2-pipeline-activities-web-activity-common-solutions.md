<properties
  pagetitle="V2 - Pipeline Activities - Web Activities&#xD;"
  description="V2-Pipeline-Activities%2DWeb-Activity-Common-Solutions"
  service=""
  resource=""
  ms.author="dfandel"
  selfhelptype="Generic"
  supporttopicids="32740731"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="c2b6d7cf-eae2-4c9e-9bde-f9021ba698fe"
  ownershipid="AzureData_DataFactory" />
# V2 - Pipeline Activities - Web Activities

## **Recommended Steps**

If you have received an error message from web activity, reference the [ADF Troubleshooting Guide - Web Activity](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide#web-activity) for more information.

### **Some Common Errors**

* Web activities timeout with an error at 1 minute if the endpoint does not send a response. Verify that the endpoint is responding to requests by using [Fiddler or Postman](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide#more-details). (If you use a Self-Hosted IR, you must validate from the IR machine.) You can also implement a [202 response](https://docs.microsoft.com/azure/architecture/patterns/async-request-reply) as suggested [here](https://docs.microsoft.com/azure/data-factory/control-flow-webhook-activity#additional-notes)

* [Error Code 2128](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide#error-code-2128-1) and [Error Code 2108](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide#error-code-2108-1) indicate connection issues with the endpoint. Debug these using [Fiddler](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide#more-details).
  
* Payload too large error: Web Activity has a limit of 4 MB HTTP Response output. This is a known limitation of web activity. As an alternative, use the [Rest API](https://docs.microsoft.com/azure/data-factory/connector-rest) to send HTTP requests. Set the REST dataset to the data source of the activity.

## **Recommended Documents**
*Understand your error codes*
* [Web Activity Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide#web-activity)

*Review Activities documents*
  * [Web Activity](https://docs.microsoft.com/azure/data-factory/control-flow-web-activity)
  * [Webhook Activity](https://docs.microsoft.com/azure/data-factory/control-flow-webhook-activity)
  
### **Important Notes**

* Use web activity for invoking URLs hosted in a private virtual network, and for leveraging self-hoted integration runtimes that have a line of sight to the URL endpoint. These activities are supported.

* REST endpoints that the web activity invokes must return a response of type JSON. 

**Azure Data Factory Information** 
* [Azure Data Factory Updates](https://azure.microsoft.com/updates/?query=factory)
* [Azure Data Factory Blog](https://techcommunity.microsoft.com/t5/azure-data-factory/bg-p/AzureDataFactoryBlog)
* [Azure Data Factory FAQ](https://docs.microsoft.com/azure/data-factory/frequently-asked-questions)
* [Azure Data Factory Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide)
* [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)
