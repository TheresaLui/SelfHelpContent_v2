
<properties
pageTitle="Data retention issue or question"
description="Data retention issue or question"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="yossiy"
displayorder=""
selfHelpType="generic"
supportTopicIds="32612455"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
	articleId="f38ac17f-88a0-438e-99e9-b2185ca65341"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Data retention issue or question
The default data retention period is dependent on the pricing plan your workspace is in. For example, it's 30 days in 'Per GB' pricing plan. However you can control the data retention period for workspaces in paid pricing plans. [Learn more](https://azure.microsoft.com/pricing/details/monitor/) about data retention pricing.

## **Recommended steps**
Follow the steps below to view, or change the data retention period in your workspace:<br>
**Through the Azure Portal**<br>
* From your workspace, select *Usage and estimated costs* from the left pane.
* On the *Usage and estimated costs* page, click *Data volume management* from the top of the page.
* On the pane, move the slider to increase or decrease the number of days and then click OK.<br>

**Through the Azure Resource Manager**<br>
* Data retention can be configured via [ARM template](https://docs.microsoft.com/azure/log-analytics/log-analytics-template-workspace-configuration#configure-a-log-analytics-workspace)<br><br>

**Important:**<br>
* If you are on the free pricing plan, you will not be able to modify the data retention period. To change the retention period, upgrade to a paid plan first.
* Data retention policy applies to all the data in the workspace except *AzureActivity* table, which has a minimum retention period of 90 days.<br>
## **Recommended documents**
* [Change the data retention period](https://docs.microsoft.com/azure/log-analytics/log-analytics-manage-cost-storage#change-the-data-retention-period)
* [Manage cost by controlling data volume and retention in Log Analytics](https://docs.microsoft.com/azure/log-analytics/log-analytics-manage-cost-storage)