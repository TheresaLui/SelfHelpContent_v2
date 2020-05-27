<properties
    pageTitle="Other alert types in Azure"
    description="Alert types which are not covered by other articles, usually either partially managed or not managed at all by Azure Monitor"
    infoBubbleText=""
    service="microsoft.alertsmanagement"
    resource="alerts"
    authors="yairgil"
    ms.author="yagil"
    displayOrder="1"
    articleId="alerts-crud-other"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32739773,32739801,32739802"
    resourceTags=""
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_ActionGroup"
/>

# My issue is with another alert type

There are alerts in Azure which are only partially managed, or not managed at all through Azure Monitor. 

## **Recommended Steps**

**Smart Detector alerts**

Application Insights [Smart Detector / Failure anomalies alerts](https://docs.microsoft.com/azure/azure-monitor/app/proactive-failure-diagnostics) are created automatically when an Application Insights resource is created. You can configure existing Failure Anomalies alert rules in the Azure portal.

**Alerts originated by partner monitoring tools**

Alerts created by System Center Operations Manager, Zabbix and Nagios monitoring tools [can be integrated with Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-managing-nagios-zabbix-scom), so that alerts triggered by those tools can be viewed in Azure Monitor. However, the alert rule configuration can only be viewed/edited in respective monitoring tools.  

**Azure Security Center alerts**

[Azure Security Center alerts](https://docs.microsoft.com/azure/security-center/security-center-managing-and-responding-alerts) are configured or managed through Azure Security Center and not through Azure Monitor. 

**Azure Sentinel alerts**

[Azure Sentinel alerts](https://docs.microsoft.com/azure/sentinel/tutorial-detect-threats-built-in) are created and managed through Azure Sentinel and not through Azure Monitor. 

**Azure cost management alerts**

[Azure cost management alerts](https://docs.microsoft.com/azure/cost-management-billing/costs/cost-mgt-alerts-monitor-usage-spending) are created and managed through Azure Cost Management and not through Azure Monitor. 

## **Recommended Documents**

* [Smart Detector / Failure anomalies alerts](https://docs.microsoft.com/azure/azure-monitor/app/proactive-failure-diagnostics#configure-alerts)
* [Manage alerts from System Center Operations Manager, Zabbix and Nagios in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-managing-nagios-zabbix-scom)
* [Manage and respond to security alerts in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-managing-and-responding-alerts)
* [Azure Sentinel alerts](https://docs.microsoft.com/azure/sentinel/tutorial-detect-threats-built-in)
* [Use cost alerts to monitor usage and spending](https://docs.microsoft.com/azure/cost-management-billing/costs/cost-mgt-alerts-monitor-usage-spending)
