<properties
    pageTitle="I have configured Azure AD logs to be routed to my storage account and don’t see all the logs"
    description="I have configured Azure AD logs to be routed to my storage account and don’t see all the logs"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="MarkusVi"
    ms.author="markvi"
    displayOrder="9"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="azureadrreports_missingdata_audit,azureadrreports_missingdata_signin"
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="active-directory-reporting-troubleshoot-audit-logs-storage-acct-mooncake"
	ownershipId="AzureIdentity_User"
/>

# I have configured Azure AD logs to be routed to my storage account and don’t see all the logs

## **Recommended Steps**

You configured the Azure AD Logs through Diagnostics settings (using the **Export Data** command) in **Azure Active Directory** > **Activity Logs** > **Audit**. Now you can't see all the sign-ins in Storage account or Event hub. The average latency for seeing the logs from the time you configured the settings is 10 minutes.

Did you:

* Check the Azure AD portal for Activity logs to see if logs are showing up there
* Check your Storage and Event Hub after 15 minutes to see if the logs showed up

If the logs don’t show up within 2 hours (SLA timelines), please file a support ticket with your Tenant ID so we can look into it. If there are certain audit logs missing in the stream, but that show up in the Azure AD portal, please provide the Date (in UTC) and CorrelationID for those logs (as samples).

## **Recommended Documents**

* [Azure Active Directory reporting latencies](https://docs.azure.cn/active-directory/reports-monitoring/reference-reports-latencies)