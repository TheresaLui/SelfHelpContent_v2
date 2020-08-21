
<properties
    pageTitle="Office 365 solution"
    description="Office 365 solution"
    service="microsoft.operationalinsights"
    resource="operationalinsightsaccounts"
    authors="morshabi"
	ms.author="moshabi"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32612494"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="fcfd10a1-34df-47aa-a9eb-989379a6bcdf"
	ownershipId="AzureMonitoring_LogAnalytics"
/>


# Office 365 Solution
**I’ve tried to on board the office 365 solution without success**

## **Recommended Steps**

The recommended way to import your Office management logs from Office 365 to Log Analytics in public Azure environment , is by using the [Office 365 connector](https://docs.microsoft.com/azure/sentinel/connect-office-365) in Microsoft’s new Azure Sentinel SIEM solution. This solution provides a better experience for collecting SharePoint and Exchange logs. To connect Azure AD logs, use the [Azure Sentinel Azure AD connector](https://docs.microsoft.com/azure/sentinel/connect-azure-active-directory), which provides richer log data than the Office 365 management logs. 

## **Recommended Documents**

* [Azure Sentinel Office 365 connector](https://docs.microsoft.com/azure/sentinel/connect-office-365)
* [Azure Sentinel Azure AD connector](https://docs.microsoft.com/azure/sentinel/connect-azure-active-directory) 