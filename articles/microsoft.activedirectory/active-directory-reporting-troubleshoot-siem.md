<properties
    pageTitle="I can't integrate Azure AD activity logs with my SIEM system"
    description="Can I integrate Azure AD activity logs with my SIEM system?"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="MarkusVi"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="azureadrreports_missingdata_audit,azureadrreports_missingdata_signin"
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="ee92f907-7be5-495a-a5c5-2e4ebc87c80f"
	ownershipId="AzureIdentity_User"
/>

# I can't integrate Azure AD activity logs with my SIEM system

## **Recommended steps**

There are two supported methods to accomplish this task:

- You can use Azure Monitor Event Hub to stream logs into your SIEM. Use the following steps to complete this task:
  - Go to Activity Logs > Sign-ins > Export Data Settings
  - Configure the logs you want to route and select the Event hub it should be routed to
  - [Setup your SIEM tool](https://docs.microsoft.com/azure/active-directory/reports-monitoring/quickstart-azure-monitor-stream-logs-to-event-hub#access-data-from-your-event-hub) with the configured Event hub
- You can use the Reporting Graph API to get the data, and then push it into your SIEM tool using your own scripts

## **Recommended documents**

- [Route Azure AD logs to Event hub](https://docs.microsoft.com/azure/active-directory/reports-monitoring/quickstart-azure-monitor-stream-logs-to-event-hub)<br>
- [Integrate AD logs through Event hub with your SIEM tool](https://docs.microsoft.com/azure/active-directory/reports-monitoring/quickstart-azure-monitor-stream-logs-to-event-hub#access-data-from-your-event-hub)<br>
- [Supported SIEM tools](https://docs.microsoft.com/azure/active-directory/reports-monitoring/overview-activity-logs-in-azure-monitor#frequently-asked-questions)<br>
- [Azure Active Directory report retention policies](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-retention)<br>
- [Getting started with the reporting API](https://docs.microsoft.com/azure/active-directory/active-directory-reporting-api-getting-started)
