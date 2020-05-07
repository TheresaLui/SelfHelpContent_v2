<properties 
    pageTitle="How do I setup the Application Insights API?"
    description="Explain how to configure the API"
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="5bcae984-826e-4880-b0eb-7498f98d76be"
    displayOrder="103"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32602213"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# How do I setup the Application Insights API?

## **Recommended Steps**

The [Application Insights API](https://dev.applicationinsights.io/) provides a REST interface to retrieve data from your Analytics source. This document will give steps to setup the feature and to troubleshoot our most common issues, such as authentication and query errors. Likely you can see the [response code error](https://dev.applicationinsights.io/documentation/Using-the-API/Errors) from your application or testing tool, and can quickly resolve the issue on your own.<br>

**Key Authentication**<br>

1. Check to make sure you've [created a key](https://dev.applicationinsights.io/documentation/Authorization/API-key-and-App-ID)
2. Ensure the Key is not expired
3. Review the [API Key documentation](https://dev.applicationinsights.io/documentation/Authorization/API-key-authentication) and validate the header is correct

**AAD Authentication**<br>

1. Review the [setup document](https://dev.applicationinsights.io/documentation/Authorization/AAD-Application-Setup)
2. Ensure the AAD Application has the correct permissions
3. Test your AAD Authentication using PostMan or another REST API tool
4. Review the [AAD Auth](https://dev.applicationinsights.io/documentation/Authorization/AAD-OAuth2-Flows) document

**General Types of Errors**<br>

* [Server Timeouts](https://dev.applicationinsights.io/documentation/Using-the-API/Timeouts)
* [Specific Response Code Errors](https://dev.applicationinsights.io/documentation/Using-the-API/Errors)

## **Recommended Documents**

* [API Overview](https://dev.applicationinsights.io/documentation/Overview)
* [Specific Response Code Errors](https://dev.applicationinsights.io/documentation/Using-the-API/Errors)
