<properties 
    pageTitle="I should have received a webhook for an alert that fired"
    description="Specific webhook guidance."
    infoBubbleText="We have seen that there is an error with one of your webhook endpoints."
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    articleId="insights_webhook_diagnostic"
    diagnosticScenario="ApplicationInsightsMissingEmailDiagnostic"
    selfHelpType="diagnostics"
    productPesIds="15693" 
    supportTopicIds="32546625"
    cloudEnvironments="public"
 />
# I should have received a webhook for an alert that fired

We have identified that the **<!--$resourcename-->[resourcename]<!--/$resourcename-->** resource has an error when sending the following webhooks between **<!--$starttime-->[starttime]<!--/$starttime-->** and **<!--$endtime-->[endtime]<!--/$endtime-->**. Note: we have limited it to the top 5.

<!--$webhooktable-->[webhooktable]<!--/$webhooktable-->

## **Recommended steps**
Please review this list of error codes 

### 400 Error Code
This error code indicates that either the URL, or payload being sent to your endpoint is invalid. 

1. Verify that the URL address you have specified for this webhook is well-formed. 
2. Verify that your endpoint is able to accept the [predefined payload](https://docs.microsoft.com/azure/monitoring-and-diagnostics/insights-webhooks-alerts#payload-schema).

### 401 Error Code
This error code indicates that there is some form of authentication assigned to that endpoint. The webhooks can only use token based authentication that is specified inside of the URL. Please see [this](https://docs.microsoft.com/azure/monitoring-and-diagnostics/insights-webhooks-alerts#authenticate-the-webhook) document for more information.

### 403 Error Code
This error code indicates that there is some form of authorization error with the authenticaiton mechanism. For example the token provided is valid, but does not have access to the endpoint. Please see [this](https://docs.microsoft.com/azure/monitoring-and-diagnostics/insights-webhooks-alerts#authenticate-the-webhook) document for more information.

### 404 Error Code
This error code indicates that the endpoint is not found. Please verify that the URL that is entered is valid and reachable.

### 499 Error Code
This error code indicates that the endpoint is throttling connections. This issue usually means that there is too much traffic being sent to either the host or the direct endpoint. If you use a singular endpoint but have had a lot of alert activations it would be highly likely this mechanism was enabled to reduce load.

### 500 Error Code
This error code indicates that there is a server side error that was unexpected by Application Insights. You must review your server logs to research this error. 

### 502 Error Code
This error code indicates that there is a problem with the gateway (web server front end, proxy, or load balancer) making connections to the back-end service. You must review your server logs to research this error. 

### 503 Error Code
This error code indicates that there is a problem with the back-end service and it is not responding to requests from the gateway (web server front end, proxy, or load balancer). TYou must review your server logs to research this error. 

### Timeout
When you see a timeout value this means that the endpoint did not respond within 2 minutes. You should check to ensure the service hosting your webhook was operational at that time.

### Client
When you see the client error this means that the Application Insights service was unable to complete the request due to a local issue. This can range from a number of causes, with the most common issue being resource exhaustion.