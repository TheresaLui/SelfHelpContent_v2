<properties
    pageTitle="V2 - Pipeline Activities - Web Activity Common Solutions"
    description="V2 - Pipeline Activities - Web Activity Common Solutions"
    service=""
    resource=""
    authors="Vimal Sharma"
    ms.author="vimals"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32740731"
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="c2b6d7cf-eae2-4c9e-9bde-f9021ba698fe"
	ownershipId="AzureData_DataFactory"
/>

# V2 - Pipeline Activities - Web Activities

## **Recommended Steps**

If you have received an error message from web activity, please reference [ADF Troubleshooting Guide - Web Activity](https://docs.microsoft.com/en-us/azure/data-factory/data-factory-troubleshoot-guide#web-activity) for more information.

## **Some Common Errors**

* No response from the endpoint. Possible causes: network connectivity, DNS failure, server certificate validation or timeout.[Error Code 2128](https://docs.microsoft.com/en-us/azure/data-factory/data-factory-troubleshoot-guide#error-code-2128-1)

* Error calling the endpoint '%url;'. Response status code: '%code;'[Error Code 2108](https://docs.microsoft.com/en-us/azure/data-factory/data-factory-troubleshoot-guide#error-code-2108-1)


## **Recommended Documents**

* [Web Activity Troubleshooting Guide](https://docs.microsoft.com/en-us/azure/data-factory/data-factory-troubleshoot-guide#web-activity) __please read to understand your error codes__ <br>

* Activities Documents, including: <br>
  * Web Activity [Supported Authentication Types](https://docs.microsoft.com/en-us/azure/data-factory/control-flow-web-activity#authentication) <br>
  * Web Activity [Request Payload Schema](https://docs.microsoft.com/en-us/azure/data-factory/control-flow-web-activity#request-payload-schema) <br>
  

## **Important Note**

* Web Activity is supported for invoking URLs that are hosted in a private virtual network as well by leveraging self-hosted integration runtime. The integration runtime should have a line of sight to the URL endpoint.

* REST endpoints that the web activity invokes must return a response of type JSON. **The activity will timeout at 1 minute with an error if it does not receive a response from the endpoint.** Please validate the endpoint is responding by using [Fiddler](https://docs.microsoft.com/en-us/azure/data-factory/data-factory-troubleshoot-guide#more-details)