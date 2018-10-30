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

### 400 Error Code
This error code indicates that either the URL, or payload being sent to your endpoint is invalid. 

1. Verify that the URL address you have specified for this webhook is well-formed. 
2. Verify that your endpoint is able to accept the [predefined payload](https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/insights-webhooks-alerts#payload-schema).

### 401 Error Code
This error code indicates that there is some form of authentication assigned to that endpoint. The webhooks can only use token based authentication that is specified inside of the URL. Please see [this](https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/insights-webhooks-alerts#authenticate-the-webhook) document for more information.

### 403 Error Code
This error code indicates that there is some form of authorization error with the authenticaiton mechanism. For example the token provided is valid, but does not have access to the endpoint. Please see [this](https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/insights-webhooks-alerts#authenticate-the-webhook) document for more information.

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

## **Recommended documents**
[Application Insights Webhook](https://support.office.com/article/overview-of-the-junk-email-filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089)<br>
[Gmail SPAM Settings](https://support.google.com/mail/answer/6579?hl=en)<br>
### E-Mail Server
[O365 Safe Sender](https://docs.microsoft.com/office365/SecurityCompliance/create-organization-wide-safe-sender-or-blocked-sender-lists-in-office-365)<br>
[Exchange SPAM Quarantine](https://docs.microsoft.com/Exchange/antispam-and-antimalware/antispam-protection/spam-quarantine)<br>
[Exchange Sender Filtering](https://docs.microsoft.com/Exchange/antispam-and-antimalware/antispam-protection/sender-filtering)<br>
[G Suite Approved Sender Settings](https://support.google.com/a/answer/2368132)<br>
### Distribution List
[Exchange Delivery Restrictions](https://docs.microsoft.com/Exchange/recipients/user-mailboxes/message-delivery-restrictions#use-the-eac-to-place-message-delivery-restrictions)<br>
[G Suite Groups External Members](https://support.google.com/a/answer/167097)<br>
### Security Appliance
[Barracuda Whitelist Settings](https://campus.barracuda.com/product/websecurityservice/doc/6553671/whitelist-and-blacklist-rules/)<br>
[Cisco Whitelist Settings](https://www.cisco.com/c/en/us/support/docs/security/email-security-appliance/118585-qa-esa-00.html)<br>

