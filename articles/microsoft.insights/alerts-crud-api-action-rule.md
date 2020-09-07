<properties
    pageTitle="I am having issues managing action rules with API, CLI or ARM template"
    description="I am having issues managing action rules with API, CLI or ARM template"
    infoBubbleText=""
    service="microsoft.alertsmanagement"
    resource="actionRules"
    authors="ofirmanor"
    ms.author="ofmanor"
    displayOrder="8"
    articleId="alerts-crud-api-action-rule"
    selfHelpType="generic"
    supportTopicIds="32739763"
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_ActionGroup"
/>

# Issues with managing action rules via API, CLI or ARM template

## **Recommended Steps**

If you are receiving an error while working with [action rules](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules) using the API, CLI or ARM templates, follow these steps:

### Are you receiving a permission error?

Ensure you have the permissions to author the action rule. Usually, you would use the ["Monitoring Contributor"](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-contributor) built-in role.

### Are you using PowerShell?

Follow the documentation on how to [get](https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azactionrule), [create](https://docs.microsoft.com/powershell/module/az.alertsmanagement/Set-AzActionRule), [update](https://docs.microsoft.com/powershell/module/az.alertsmanagement/update-azactionrule), or [delete](https://docs.microsoft.com/powershell/module/az.alertsmanagement/remove-azactionrule) an action rule using the [Az module](https://docs.microsoft.com/powershell/azure/new-azureps-module-az).

## **Recommended Documents**

* [Creating and managing action rules](https://docs.microsoft.com/powershell/module/az.alertsmanagement/Set-AzActionRule?view=azps-3.8.0)<br>
