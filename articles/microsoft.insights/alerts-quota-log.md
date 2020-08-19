<properties
  pagetitle="I want to increase my log search alerts quota"
  service="microsoft.insights"
  resource="scheduledqueryrules"
  ms.author="yalavi,yagil"
  selfhelptype="Generic"
  supporttopicids="32739787,32745407"
  resourcetags=""
  productpesids="15454,15725"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="alerts-quota-log"
  ownershipid="AzureMonitoring_Alerts_LogSearchAlerts" />
# I want to increase my log search alerts quota

The number of log search alert rules per subscription and resource are subject to the quota limits described [here](https://docs.microsoft.com/azure/azure-monitor/service-limits).

## **Recommended Steps**
    
If you have reached the quota limit, the following steps may help resolve the issue:

1. Try deleting or disabling log search alert rules that aren’t used anymore
2. If you need the quota limit to be increased, please proceed to open a support request, and provide the following information:

    - Subscription Id(s) for which the quota limit need to be increased
    - Reason for quota increase
    - Resource type for the quota increase: **Log Analytics**, **Application Insights** etc
    - Requested quota limit

To check the current usage of new log alert rules:
	
### **From the Azure portal**

1. Open the *Alerts* screen, and click *Manage alert rules*
2. Filter to the relevant subscription using the *Subscription* dropdown control
3. Make sure NOT to filter to a specific resource group, resource type or resource
4. In the *Signal type* dropdown control, select 'Log Search'
5. Verify that the *Status* dropdown control is set to ‘Enabled’
6. The total number of log search alert rules will be displayed above the rules list

### **From API**

- PowerShell: [Get-AzScheduledQueryRule](https://docs.microsoft.com/powershell/module/az.monitor/get-azscheduledqueryrule?view=azps-3.7.0)
- REST API: [List by subscription](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules/listbysubscription)