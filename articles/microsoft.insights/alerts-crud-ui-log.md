<properties
  pagetitle="I am having issues creating, editing, or deleting log alert rules"
  service="microsoft.insights"
  resource="scheduledqueryrules"
  ms.author="yalavi,aaronmax"
  selfhelptype="Generic"
  supporttopicids="32739785,32612472"
  resourcetags=""
  productpesids="15454,15725"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="alerts-crud-ui-log"
  ownershipid="AzureMonitoring_Alerts_LogSearchAlerts" />
# I am having issues creating, editing, or deleting log alert rules

[Log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log) run your analytics queries against the data available on [Azure Monitor Logs](https://docs.microsoft.com/azure/azure-monitor/log-query/query-language) or [Application Insights logs](https://docs.microsoft.com/azure/azure-monitor/app/analytics).

## **Recommended Steps**

If you are running into issues while creating, editing, or deleting log alert rules, the following steps may help resolve the issue.

1. If you don't know how to write the query, start the creation from log analytics:

    * Go to the resource you would like to alert on
    * Under **Monitor**, select **Logs**
    * Query the log data that can indicate the issue. You can use examples to understand what you can discover or [get started on writing queries](https://docs.microsoft.com/azure/azure-monitor/log-query/get-started-portal). Also, [learn how to create optimized alert queries](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log-query).
    * Press on '+ New Alert Rule' button to start the alert creation flow

1. Review the query to ensure you are using analytics commands compatible with log alert:

    * Alerting service executes the provided analytics query repeatedly at the frequency specified, therefore, usage of certain analytics commands with high overhead are not permitted. [Understand the unsupported commands and alternatives](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log-query) to construct query for log alerts correctly.
    * [Log alert of type metric measurement](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log#metric-measurement-alert-rules) trigger when a metric value computed in query crosses the threshold specified. Since a query can have multiple metric computations, you are required to name the specific computation to be used as *AggregatedValue* and use the *bin* command to aggregate the metric over required time.
    * Log alert rules with [cross-resource query, group field aggregation selection, and period of up to 48 hours](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log-api-switch#benefits-of-switching-to-new-azure-api) are available in Azure portal, only after you [switch to use the new ScheduledQueryRules API](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log-api-switch)

1. Ensure that the various options for log alert rule have been configured:

    * Configuring alert rules in Azure Monitor requires you to specify the resource, condition, action groups and alert details. Each of the section requires parameters and variables to be chosen, you can [review tutorial on creating log alerts in Azure portal](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log#managing-log-alerts-from-the-azure-portal) to understand each section and variable better. And set them correctly to allow alert rule creation without errors or issues.
    * Log alert rules which are invalid will get disabled by Azure Monitor. [Understand the reasons why alert would get disabled and how to its communicated](https://docs.microsoft.com/azure/azure-monitor/platform/alert-log-troubleshoot#log-alert-was-disabled). If your alert rule is disabled, it will be still available in Azure Monitor and [the rules can be managed or edited in Azure portal](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log#view--manage-log-alerts-in-azure-portal).

1. Hidden alert rules creation for billing cannot be deleted:

    * For billing of alerts created via legacy means, hidden pseudo alert rules are made on `microsoft.insights/scheduledqueryrules` as shown as `<WorkspaceName>|<savedSearchId>|<scheduleId>|<ActionId>` along with resource group and alert properties. To understand the need for these hidden alert rules and how to remove them, see article on [billing of log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log#pricing-and-billing-of-log-alerts).

1. Alert rule creation or modification can be done only if user has appropriate rights and permissions:

    * Azure Monitor has built-in role named [Monitoring Contributor](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-contributor) to help limit access to resources while still enabling those responsible for monitoring infrastructure to obtain and configure alert rules
    * To create log alert rules, a user must have [Monitoring Contributor Role](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-contributor) or [custom RBAC role with access to write operation](https://docs.microsoft.com/azure/azure-monitor/platform/roles-permissions-security#monitoring-permissions-and-custom-rbac-roles) for Microsoft.Insights/ScheduledQueryRules

### **Advisory and How-To**
[![Monitoring Video](https://docs.microsoft.com/azure/azure-monitor/app/media/troubleshoot/alerts/how-to-configure-an-alert-rule.png)](https://www.microsoft.com/videoplayer/embed/RE4tflw?autoplay=1)


## **Recommended Documents**

* [View/edit log alerts](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-log)
* [Understanding how log alerts work](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-unified-log)
* [Troubleshoot deployment with Azure Resource Manager](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors)