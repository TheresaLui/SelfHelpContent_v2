<properties 
    pageTitle="I need help configuring Application Insights using PowerShell"
    description="General troubleshooting guide for PowerShell"
    service="microsoft.insights"
    resource="components"
    authors="debugthings,osvaldorosado"
    ms.author="jamdavi"
    articleId="insights-powershell"
    displayOrder="97"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32602216,32632995,32729591"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# I need help using PowerShell to automate my Application Insights deployments

Most of our cmdlets work by calling an ARM endpoint and should work so long as you have access to the resource or the subscription. Below are the most common questions we get with PowerShell and Application Insights.<br>

**How can I automate with operations on Application Insights resources with PowerShell?**

Application Insights has a variety of PowerShell cmdlets that help automate common interactions with the service:

* To create a new resource use **New-AzApplicationInsights** or **Remove-AzApplicationInsights** to delete one 
* To manage your Application Insights resource’s daily cap using **Get-AzApplicationInsights -IncludeDailyCap** to retrieve the current value, or **Set-AzApplicationInsightsDailyCap** to set a new cap
* To manage your Application Insights resource’s Continuous Export rules, use **Get-AzApplicationInsightsContinuousExport**, **Set-AzApplicationInsightsContinuousExport**, **New-AzApplicationInsightsContinuousExport**, and **Remove-AzApplicationInsightsContinuousExport**
* To manage your Application Insights resource’s API keys using **Get-AzApplicationInsightsApiKey**, **New-AzApplicationInsightsApiKey**, and **Remove-AzApplicationInsightsApiKey**

Review the [Manage Application Insights using PowerShell](https://docs.microsoft.com/azure/azure-monitor/app/powershell) doc for more information.

**How to work with Application Insights resources using an ARM template?**<br>

1. Review the [Deploy resources with templates](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-template-deploy) guide
2. Review the [Create Application Insights resources using an ARM template](https://docs.microsoft.com/azure/azure-monitor/app/powershell#create-application-insights-resources-using-a-resource-manager-template) doc

**How do I troubleshoot issues using the Application Insights ARM template?**

If you’re getting an error using the Application Insights ARM template, [this page](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors) will guide you through steps to understand and mitigate the error. 

## **Recommended Documents**

* [Deploy resources with templates](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-template-deploy)
* [Manage Application Insights using PowerShell](https://docs.microsoft.com/azure/azure-monitor/app/powershell)
* [Create Application Insights resources using an ARM template](https://docs.microsoft.com/azure/azure-monitor/app/powershell#create-application-insights-resources-using-a-resource-manager-template)
* [Deployment Errors](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors)
