<properties
    pageTitle="Problem with Azure AD logs in Azure Monitor "
    description="Azure AD reporting"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="dhanyahk"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32574686"
    resourceTags=""
    productPesIds="16577"
    cloudEnvironments="public"
    />

# Azure AD audit Logs

## **Recommended steps**

* Sign-ins are available only for Azure AD Premium-licensed tenants. It's not available for Free- or Basic-licensed tenants.
* Audit and Sign-ins logs are only available from the time you have configured the logs to be routed through Azure Monitor Diagnostics. There's no backfilling of the logs.

### **Troubleshooting issues with sign-ins**

If you are a P1 tenant and can't see the sign-ins within 15 mins in the destination you configured (Storage Account or Event Hub or Log Analytics WOrkspace), file a support ticket if the delay exceeds the documented latency

## **Recommended documents**

* [Azure AD Logs in Azure Monitor](https://docs.microsoft.com/azure/active-directory/reports-monitoring/concept-activity-logs-azure-monitor)<br>
* [Azure AD Activity Logs Latency](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-reports-latencies)  
